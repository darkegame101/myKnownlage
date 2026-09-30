# Domain: Computer Networking & Network Programming — Summary

## Current Level Assessment
- **Java Network Socket Programming**: 3/5 (Theory: 3/5, Practical: 3/5, Troubleshooting: 2/5, Design: 2/5) — *Verified via Java Chat Room & Remote Desktop projects.*
- **Computer Networking Infrastructure & Protocols**: 2/5 (Theory: 3/5, Practical: 1/5, Troubleshooting: 1/5, Design: 2/5) — *Evidence: Partial (Theory of TLS 1.3, ECDHE, QUIC, HTTP/3 consolidated; packet capture & routing lab pending P003).*

> ⚠️ **Critical Distinction**: Completing Java Network Socket Programming (`Socket`, `ServerSocket`, `DatagramPacket`) does **NOT** equal mastering Computer Networking Infrastructure (CIDR Subnetting, ARP, Routing, NAT, IP Forwarding, Wireshark packet capture).

---

## What I Have Learned

### 1. Java Network Programming (Verified)
- Client-Server network architecture, IP Address representation in Java (`InetAddress`).
- Java `URL` and `URLConnection` web resource fetching.
- Multithreaded socket servers (`Thread`, `Runnable`, `synchronized` state protection, Producer-Consumer pattern).
- Java TCP Socket Programming (`Socket`, `ServerSocket`), Multi-client Chat Room server, Remote Desktop GUI project.
- Java UDP Datagram Programming (`DatagramSocket`, `DatagramPacket`), UDP DNS simulator project.
- Java Multicast Programming (`MulticastSocket`), Lightstick controller simulation.
- Java Remote Method Invocation (RMI) distributed objects introduction.

### 2. Web Protocols, TLS Security & Modern Transport (Consolidated Theory — Level 3/5)
- **HTTP, HTTPS & TLS Fundamentals**:
  - HTTP request/response model; HTTPS as HTTP over TLS.
  - The 4 core responsibilities of TLS: Authentication, Key exchange, Encryption, Integrity.
  - Why HTTPS does not simply use public key encryption for bulk HTTP data (asymmetric overhead vs symmetric session keys).
- **TLS 1.3 Handshake & Cryptographic Mechanics**:
  - Handshake flow: `ClientHello` + Key Share $\rightarrow$ `ServerHello`, `Certificate`, `CertificateVerify`, `Finished`.
  - Server Certificate structure (Domain, Public Key, Validity, CA Signature); Private Key secrecy.
  - CA Trust Store verification chain (Root CA $\rightarrow$ Intermediate CA $\rightarrow$ Server Certificate).
  - Difference between `Certificate` (identity claim) and `CertificateVerify` (proof of private key ownership via transcript signing).
  - Elliptic Curve Diffie-Hellman Ephemeral (ECDHE): deriving identical shared secret without transmitting secrets over the wire.
  - Symmetric bulk encryption: AES-GCM and ChaCha20-Poly1305 using derived Session Keys.
- **Java HTTPS via JSSE**:
  - `KeyStore`, `SSLContext`, `SSLServerSocket`, `SSLSocket`.
  - Application-level transparency: application receives decrypted plaintext HTTP requests.
- **HTTP Protocol Evolution & QUIC**:
  - HTTP/1.1 (TCP, text headers, Head-of-Line blocking) vs HTTP/2 (binary framing, multiplexing streams over 1 TCP connection).
  - HTTP/3 over QUIC over UDP: eliminating TCP Head-of-Line blocking between streams.
  - TCP 4-tuple identification vs QUIC 64-bit Connection ID.
  - QUIC Connection Migration: seamless network switching (Wi-Fi $\rightarrow$ 4G/5G) without connection drops.

### 3. Computer Networking Infrastructure (Tracking / Unverified Gaps)
- **Layer 2 (Data Link)**: Ethernet, MAC Addressing, ARP (`arp -a`) — *Concept 1/5, Practical 0/5*.
- **Layer 3 (Network)**: IPv4 Address structure, CIDR Subnetting (`/24`, `/16`), Routing tables, NAT (Network Address Translation), DHCP, ICMP (`ping`, `traceroute`) — *Concept 2/5, Practical 1/5*.
- **Network Diagnostics & Tools**: Wireshark, `tcpdump`, `nc` (netcat), `nmap` — *Unverified / No Evidence (0/5)* (Target of [`P003`](../00-projects/P003-network-packet-investigation.md)).

---

## Strong Areas
- Building multi-threaded Java TCP/UDP Socket network applications (Chat Room, Remote Desktop, UDP DNS simulator).
- Managing concurrent socket input/output streams and thread synchronization in Java JVM memory.

## Weak Areas
- Network Packet Analysis: Never captured or debugged live TCP handshakes or packet retransmissions using Wireshark or `tcpdump`.
- IP Routing & Subnetting: Lacking CIDR math, NAT port forwarding rules, and routing table configuration.
- Security Protocols: SSL/TLS cryptographic handshakes, HTTPS certificate verification (`SSLSocket`).

## Missing Knowledge (Tracked Gaps)
- **Computer Networking Core**: OSI 7-Layer Model, TCP/IP Model, Ethernet, MAC, ARP, IPv4, CIDR (`/24`), Routing, NAT, DHCP, ICMP.
- **Packet Analysis Tools**: Wireshark, `tcpdump`, `traceroute`, `dig`, `nc`.
- **Application & Security**: HTTP/1.1, HTTP/2, WebSockets, TLS/SSL Certificate handshakes, Firewall/ACL.

## Practical Gaps
- **Java Network Programming**: Theory 3/5, Practical 3/5.
- **Computer Networking Infrastructure**: Theory 2/5, Practical 1/5, Troubleshooting 0/5.
- **Gap**: Lacking hands-on packet capture with Wireshark/tcpdump to observe TCP 3-way handshake, packet loss retransmissions, and FIN/RST teardowns.

## Depth Gaps
- Socket Abstraction vs Packet Transport: Understood Java `Socket` API abstraction, missing lower-level IP packet structure, frame headers, and router hop mechanisms.

## Recommended Supplements
1. **Wireshark / tcpdump Lab**: Capture local TCP 3-way handshakes, HTTP GET requests, and DNS UDP packets.
2. **CIDR Subnetting & Routing**: Practice CIDR subnet math (`/24`, `/28`) and Linux routing table inspection (`ip route`).
3. **HTTP & TLS**: Study HTTP request lifecycle and TLS/SSL certificate handshakes.

## Readiness for Next Topics
- **Java Network Applications**: **READY (3/5)**
- **Docker Container Networking & Cloud VPC**: **NOT READY (1/5)**
  - Java Socket API: 3/5
  - Computer Networking (CIDR, NAT, ARP, Routing): 1/5
  - Linux Network Namespaces & Bridges: 1/5
  - *Reason*: Docker networking and Cloud VPC require solid CIDR subnetting, Linux bridge interfaces, and iptables NAT. Need to complete Computer Networking fundamentals before Docker Networking.
