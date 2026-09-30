# Assessment Instrument: P003 — Network Packet Investigation Lab

## 📌 Project Overview
- **Project ID**: `P003`
- **Project Name**: Network Packet Investigation Lab
- **Domain**: Computer Networking Infrastructure & Diagnostics
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Practical 3/5, Troubleshooting 3/5, Theory 3/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Perform packet-level network investigation using Wireshark and `tcpdump` across the OSI/TCP-IP stack (Layer 2 through Layer 7), analyzing packet captures of ARP, ICMP, DNS, TCP handshakes, TLS negotiation, and HTTP/HTTPS traffic.
- **Why this project exists**: The repository records a critical distinction: *Java Socket Programming is Level 3/5, but Computer Networking Infrastructure is currently at Level 1/5*. To unlock Docker container networking, cloud VPCs, and distributed systems debugging, the student must prove hands-on mastery of raw network packets, subnetting, routing, and diagnostic tools.

---

## 📋 2. Prerequisites
- Basic OS Concepts & System Calls (Level 3/5)
- Linux CLI or Windows Terminal Navigation (Level 3/5)
- Basic Socket Programming Context ([`C006`](../00-sources/C006-java-network.md))

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- The 4-layer TCP-IP and 7-layer OSI models: encapsulation and decapsulation of headers (Ethernet Frame $\rightarrow$ IP Packet $\rightarrow$ TCP Segment $\rightarrow$ Application Payload).
- IPv4 addressing and CIDR notation: subnet masks, network address, broadcast address, valid host IP calculations.
- Address Resolution Protocol (ARP): MAC address resolution and ARP cache mechanism.
- Transmission Control Protocol (TCP): Connection establishment (3-way handshake: SYN, SYN-ACK, ACK), sequence/acknowledgment tracking, flow control (window size), connection termination (FIN-ACK vs RST).
- Domain Name System (DNS) query/response structure and Transport Layer Security (TLS 1.2/1.3) cryptographic handshake.

### B. Practical Skills Assessed
- Capturing traffic on specific network interfaces using `tcpdump` (CLI) and Wireshark (GUI).
- Filtering packet captures using Wireshark display filters (`ip.addr == ...`, `tcp.flags.syn == 1`, `dns`, `http`).
- Calculating CIDR subnets and verifying local routing tables (`ip route` or `netstat -rn`).

### C. Troubleshooting Skills Assessed
- Diagnosing network latency and packet loss using ICMP `ping` and MTU fragmentation issues (`ping -M do -s ...`).
- Tracing packet hops and detecting routing loops using `traceroute` / `tracert`.
- Identifying TCP connection reset issues (`RST` flag) and packet retransmissions in Wireshark.

### D. Design Skills Assessed
- Designing an IP subnet scheme for an enterprise network dividing a `/16` block into isolated functional subnets (`/24` for servers, `/26` for databases, `/24` for DMZ).

---

## 🧪 4. Required Hands-on Packet Captures & Experiments

All experiments must produce `.pcapng` capture files and terminal logs placed in an `evidence/` directory:

### Investigation 1: Layer 2 ARP Inspection (`evidence/arp_capture.pcapng`)
1. Clear the local ARP table (`ip -s -s neigh flush all` on Linux or `arp -d *` on Windows).
2. Ping a local gateway or LAN host.
3. Capture the broadcast `ARP Request` ("Who has 192.168.1.1? Tell 192.168.1.X") and the unicast `ARP Reply`.
4. Document the source MAC, destination broadcast MAC (`ff:ff:ff:ff:ff:ff`), and ARP cache entry.

### Investigation 2: ICMP & TTL Expiration (`evidence/icmp_traceroute.pcapng`)
1. Execute `traceroute -I 8.8.8.8` (or `tracert 8.8.8.8`).
2. Capture ICMP Echo Request packets with `TTL = 1, 2, 3...`.
3. Capture the resulting `ICMP Time-to-Live exceeded in transit` (Type 11, Code 0) packets returned by intermediate routers.

### Investigation 3: TCP 3-Way Handshake & Teardown (`evidence/tcp_handshake.pcapng`)
1. Start Wireshark filter: `tcp.port == 80 || tcp.port == 8080`.
2. Connect to an HTTP web server or custom Java Socket server.
3. Identify and annotate the exact 3 packets:
   - Packet 1: `[SYN]` Seq=0, Win=65535, MSS=1460
   - Packet 2: `[SYN, ACK]` Seq=0, Ack=1
   - Packet 3: `[ACK]` Seq=1, Ack=1
4. Identify the 4-way teardown sequence (`FIN, ACK` $\rightarrow$ `ACK` $\rightarrow$ `FIN, ACK` $\rightarrow$ `ACK`) or immediate abort via `[RST, ACK]`.

### Investigation 4: DNS Resolution (`evidence/dns_lookup.pcapng`)
1. Run `dig @8.8.8.8 example.com` or `nslookup example.com`.
2. Capture UDP datagram over port 53.
3. Annotate the DNS Query (Query Type: A, Class: IN) and DNS Answer record (IPv4 address, TTL).

### Investigation 5: TLS 1.3 Cryptographic Handshake (`evidence/tls_handshake.pcapng`)
1. Navigate to an HTTPS website (`https://curl.se`).
2. Capture the TLS exchange:
   - Identify `Client Hello`: Client Random, supported cipher suites, SNI (Server Name Indication).
   - Identify `Server Hello`: Server Random, selected cipher suite.
   - Explain why subsequent HTTP request/response payloads appear as `Application Data` (encrypted).

### Investigation 6: CIDR Subnetting Problem Set (`evidence/subnetting_worksheet.md`)
Solve and explain with binary arithmetic:
- Given network block `10.100.0.0/16`:
  - Create 4 subnets of size 500 hosts each.
  - State the CIDR prefix, subnet mask, network ID, first usable IP, last usable IP, and broadcast address for each subnet.

---

## 🛑 5. Acceptance Criteria

| Skill Area | Minimum Required Evidence | Advanced Proof |
| :--- | :--- | :--- |
| **Wireshark Analysis** | Captured `.pcapng` files showing ARP, ICMP, DNS, TCP Handshake with annotated screenshots. | Following TCP streams and reassembling segmented payloads. |
| **TCP Internals** | Clear technical explanation of relative vs raw sequence numbers and TCP Window scaling. | Capturing a simulated packet loss scenario showing TCP Retransmission. |
| **CIDR & Subnetting** | Accurate binary calculation of subnet boundaries and broadcast addresses. | Verification of host reachability across subnets via routing table configuration. |
| **Command-Line Capture** | Capturing traffic using CLI `tcpdump -i any -nn -w capture.pcap 'tcp port 80'` on a Linux terminal. | Using `tshark` to parse and extract specific fields via terminal script. |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove mastery of BGP / OSPF dynamic routing protocol configurations.
- Does **NOT** prove enterprise Cisco switch VLAN trunking (`802.1Q`).
- Does **NOT** prove kernel-level socket driver development.

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed packet lab to AI for assessment:*

```markdown
Project ID: P003
Project Name: Network Packet Investigation Lab
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Packet Captures Submitted
- Layer 2 ARP capture: [File path in repo]
- ICMP TTL Expiration capture: [File path in repo]
- TCP 3-Way Handshake capture: [File path in repo]
- DNS Resolution capture: [File path in repo]
- TLS Handshake capture: [File path in repo]

### 2. TCP Protocol Verification
- Annotated SYN, SYN-ACK, ACK packet sequence numbers:
- How TCP Teardown occurred (FIN vs RST):

### 3. CIDR Subnet Calculations
- Subnetting worksheet link:
- How broadcast and network IDs were validated:

### 4. Diagnostic Scenarios Tested
- Tools used: [Wireshark version, tcpdump, ping, traceroute, dig]
- Unusual network anomalies observed:
```
