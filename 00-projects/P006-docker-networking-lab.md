# Assessment Instrument: P006 — Docker Networking Lab

## 📌 Project Overview
- **Project ID**: `P006`
- **Project Name**: Docker Networking Lab
- **Domain**: Containerization & Operating System Networking
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Practical 4/5, Troubleshooting 4/5, Theory 4/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Demystify container networking by connecting Linux networking primitives (network namespaces, `veth` pairs, bridge devices, `iptables` NAT) directly to Docker's default and user-defined bridge networks, proving container-to-container DNS resolution, port forwarding mechanics, and capturing container traffic with `tcpdump`.
- **Why this project exists**: Anyone can execute `docker run -p 8080:80 nginx`. However, in real production environments and Kubernetes clusters, container issues manifest as packet drops, DNS timeouts, and routing failures. This assessment ensures the student does **not** treat Docker as a black box, but understands how Docker orchestrates the underlying Linux networking primitives.

---

## 📋 2. Prerequisites
- Computer Networking Fundamentals (CIDR, ARP, Routing, NAT) ([`P003`](./P003-network-packet-investigation.md))
- Linux Systems & Network Namespaces ([`P004`](./P004-linux-diagnostics.md))
- Basic Docker Engine Installation & CLI Commands (Level 2/5)

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- The Container Network Model (CNM): Network Sandbox (Network Namespace), Endpoint (`veth`), and Network (Linux Bridge).
- Default Bridge (`bridge` / `docker0`) vs User-Defined Custom Bridge: Why automatic container name DNS resolution is disabled on the default bridge and enabled on user-defined networks.
- Port Publishing Mechanics (`-p`): The dual roles of user-space `docker-proxy` and kernel-space `iptables` DNAT (Destination NAT).
- Outbound Container Traffic: Source NAT (SNAT / IP MASQUERADE) through the host's physical network interface.

### B. Practical Skills Assessed
- Inspecting Docker network drivers: `docker network ls`, `docker network inspect <net_name>`.
- Creating user-defined bridge networks with custom subnets (`--subnet 172.28.0.0/16`).
- Inspecting hidden container network namespaces in `/var/run/netns` using `ip netns`.
- Inspecting host `iptables` NAT rules created by Docker (`iptables -t nat -nvL DOCKER`).

### C. Troubleshooting Skills Assessed
- Diagnosing container connectivity failures using `docker exec <container> ping`, `traceroute`, `curl`, and `nslookup`.
- Capturing packets traversing the virtual bridge (`docker0` or `br-<network-id>`) using `tcpdump -i <bridge-interface> -nn`.
- Tracing packet flow from the host's physical interface through `iptables` DNAT into the container's private IP.

### D. Design Skills Assessed
- Designing isolated multi-tier network topologies using `docker-compose.yml` (e.g. `frontend-net` isolated from `backend-net`, with database container accessible only to backend services).

---

## 🧪 4. Required Hands-on Experiments

All terminal commands, network dumps, and diagnostic outputs must be recorded in markdown lab logs:

### Experiment 1: The Docker-to-Linux Mapping Inspection
1. Run a detached Nginx container: `docker run -d --name web1 -p 8080:80 nginx:alpine`.
2. Find the container's PID: `PID=$(docker inspect --format '{{.State.Pid}}' web1)`.
3. Link the container network namespace so standard Linux tools can see it:
   ```bash
   sudo mkdir -p /var/run/netns
   sudo ln -sf /proc/$PID/ns/net /var/run/netns/web1
   ```
4. Run `ip netns exec web1 ip addr`: Prove the container has its own private `eth0` interface and loopback `lo`.
5. Identify the peer `veth` interface on the host machine using `ethtool -S vethXXX` or interface index mapping. Prove that `vethXXX` is plugged into the `docker0` bridge via `brctl show` or `ip link show master docker0`.

### Experiment 2: Demystifying `-p 8080:80` Port Forwarding
1. Inspect listening ports on the host with `ss -tulpn | grep 8080`: Identify `docker-proxy`.
2. Inspect the Linux kernel NAT table:
   ```bash
   sudo iptables -t nat -nvL DOCKER
   ```
3. Locate the DNAT rule:
   - Match: Protocol TCP, Destination Port 8080
   - Target: `DNAT` to container private IP (e.g. `to:172.17.0.2:80`).
4. Explain clearly: Why does traffic still reach the container even if `docker-proxy` process is terminated? (Because the in-kernel `iptables` DNAT rule handles the packet redirection).

### Experiment 3: Default Bridge vs User-Defined Bridge DNS Resolution
1. Spin up two containers on the default bridge:
   ```bash
   docker run -d --name c1 alpine sleep 3600
   docker run -d --name c2 alpine sleep 3600
   ```
2. Run `docker exec c1 ping c2`: Prove that DNS lookup fails ("bad address 'c2'"). Explain why (default bridge only supports `--link` legacy mechanism).
3. Create a custom bridge network:
   ```bash
   docker network create --driver bridge my-isolated-net
   ```
4. Attach `c1` and `c2` to `my-isolated-net`.
5. Re-run `docker exec c1 ping c2`: Prove that name resolution succeeds immediately via Docker's embedded 127.0.0.11 DNS server.

### Experiment 4: Bridge Packet Capture with `tcpdump`
1. Identify the virtual bridge interface: `ip link show type bridge`.
2. Start capturing on the bridge:
   ```bash
   sudo tcpdump -i br-xxxx -nn -vv 'tcp port 80' -w evidence/docker_bridge.pcap
   ```
3. Send an HTTP request from `c1` to `c2`.
4. Open `docker_bridge.pcap` in Wireshark:
   - Prove that within the bridge, packets carry the private container IP addresses (`172.18.0.2` $\rightarrow$ `172.18.0.3`) without NAT.

---

## 🛑 5. Acceptance Criteria

| Criteria | Minimum Required Evidence | Advanced Proof |
| :--- | :--- | :--- |
| **Linux Primitive Mapping** | Command logs proving mapping between container `eth0`, host `veth`, and bridge device. | Diagram illustrating the network path from host eth0 $\rightarrow$ iptables $\rightarrow$ bridge $\rightarrow$ veth $\rightarrow$ container. |
| **Port Forwarding** | Documented `iptables -t nat` rule analysis demonstrating DNAT destination rewriting. | Demonstrating traffic capture before and after DNAT translation. |
| **Container DNS** | Verified test comparing default bridge failure vs custom network embedded DNS success. | Inspecting `/etc/resolv.conf` inside container pointing to `127.0.0.11`. |
| **Network Isolation** | Demonstrating two containers on separate user-defined bridges that cannot ping each other. | `docker-compose.yml` multi-tier application with isolated database network. |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove Kubernetes CNI (Calico, Flannel, Cilium) overlay routing across multiple nodes.
- Does **NOT** prove Docker Swarm overlay network with VXLAN encapsulation.

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed Docker networking lab to AI for assessment:*

```markdown
Project ID: P006
Project Name: Docker Networking Lab
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Host & Docker Environment
- Docker Engine version:
- Linux Host Kernel version:

### 2. Experiments Evidence
- Container network namespace mapping log: [File link]
- Host `iptables -t nat` inspection snippet: [File link]
- Custom bridge DNS resolution verification: [File link]
- Bridge packet capture (`.pcap` / screenshot): [File link]

### 3. Key Conceptual Understandings
- Why does the default bridge disable DNS resolution between container names?
- Exactly what happens at the packet level when a curl request hits `localhost:8080`?
```
