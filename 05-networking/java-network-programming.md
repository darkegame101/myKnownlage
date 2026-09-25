# Networking & Java Network Programming

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: High

## What I Have Learned
- **Networking & Internet Overview**:
  - Introduction to Computer Networks, Internet infrastructure, Client-Server architecture.
  - IP Address concept, IPv4 basics, Hostname resolution, DNS concept.
  - Java IP Address handling: `InetAddress` class (`getByName()`, `getLocalHost()`, `getHostAddress()`), NSLOOKUP tool project.
- **Java I/O & Multithreading for Networking**:
  - Java Stream I/O review (Byte streams, Character streams, Buffered streams).
  - Multithreading concepts: `Thread` class, `Runnable` interface, Multi-threading in networking applications.
  - Thread Synchronization: `synchronized` keyword, Race condition prevention, Producer-Consumer pattern.
  - File management & Card manager desktop application.
  - Multi-threaded Library Management Application.
- **URL & Web Data Retrieval**:
  - `URL` class, `URLConnection`, downloading HTML and web resources over HTTP in Java.
- **TCP Socket Programming**:
  - TCP Protocol concept (connection-oriented, reliable transmission).
  - Socket programming API: `Socket` (Client), `ServerSocket` (Server).
  - InputStream & OutputStream over Sockets.
  - Simple 1-on-1 Client-Server Chat Application.
  - Multi-client Chat Room Server using multithreading.
  - Remote Desktop Control Application project (sending screenshot frames, remote mouse/keyboard event handling over TCP sockets).
- **UDP Datagram Socket Programming**:
  - UDP Protocol concept (connectionless, unreliable, low-overhead Datagrams).
  - `DatagramSocket`, `DatagramPacket` class usage.
  - UDP Sender & Receiver applications.
  - Simulated UDP DNS Domain Name Resolution system project.
- **Multicast & Distributed Objects**:
  - Multicast concept, `MulticastSocket`, joining multicast groups (`joinGroup()`).
  - Multicast messaging application.
  - Lightstick control simulation via Multicast packets.
  - Distributed Object Systems: Java Remote Method Invocation (RMI) introduction (`Remote`, `UnicastRemoteObject`, RMI Registry).

## What I Understand
- Difference between TCP (connection-oriented, 3-way handshake, reliable, packet order guaranteed) and UDP (connectionless, lightweight, packet loss possible, no handshake).
- How `ServerSocket.accept()` blocks until a client connects and why multi-threading (or thread pools) is required to handle concurrent client connections.
- Thread synchronization using `synchronized` blocks/methods to prevent state corruption when multiple threads access shared resources simultaneously.
- Mechanism of IP Multicast for broadcasting data to multiple subscribers in a local network without unicasting separate packets.
- Fundamentals of Remote Method Invocation (RMI) in invoking methods on Java objects hosted on remote JVMs.

## What I Can Do
- Build multi-threaded TCP Client-Server applications in Java (Chat Room, File Transfer, Remote Desktop).
- Build UDP Datagram applications and Multicast packet broadcast/receive applications.
- Perform DNS IP lookup in Java using `InetAddress`.
- Fetch content from web URLs using Java `URLConnection`.
- Apply multithreading and `synchronized` blocks to handle concurrent network I/O.

## What I Cannot Yet Do
- Perform packet analysis using Wireshark or tcpdump to inspect TCP 3-way handshakes, sequence numbers, ACKs, retransmissions, or window sizing.
- Configure enterprise networking: CIDR Subnetting, ARP, DHCP, NAT, VLANs, BGP, OSPF, ICMP.
- Build modern Non-blocking I/O (NIO) netty/event-loop network applications.
- Configure TLS/SSL certificates (`SSLSocket`, HTTPS) over Java sockets.

## Evidence
- **Source**: TITV - Lập trình mạng (sử dụng Java)
- **URL**: [https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/)
- **Section/Lectures**: Lessons 01 to 34 (Full course completed)
- **Date learned**: Completed
- **Lab/Project**: NSLOOKUP App, TCP Chat Room App, UDP DNS Simulator, Remote Desktop GUI App, Multicast Lightstick Controller. *Practical ability verified via course projects.*

## Weaknesses
- Strong in Java Socket API programming, but lacking deep OSI 7-layer / TCP/IP packet level troubleshooting tools (Wireshark, tcpdump).
- Limited understanding of network layer fundamentals (IP Subnetting CIDR, NAT, ARP, Routing tables).

## Missing Knowledge
- **Networking Infrastructure Fundamentals**: OSI 7-Layer Model, TCP/IP Model, Subnetting & CIDR (`/24`, `/16`), ARP, DHCP, ICMP, NAT, Router vs Switch.
- **Packet Analysis Tools**: Wireshark, `tcpdump`, `traceroute`, `dig`, `nc` (netcat).
- **Security & Encryption**: TLS/SSL Handshake, HTTPS, Public/Private Key Cryptography, Certificates.

## Recommended Supplement
1. Study TCP/IP stack fundamentals: Subnetting (CIDR), NAT, ARP, Routing.
2. Practice capturing TCP handshakes and HTTP traffic using Wireshark or `tcpdump`.
3. Learn Java Non-blocking I/O (NIO / `java.nio.channels.SocketChannel`).
