# Master Knowledge & Practical Gap Analysis

Comprehensive identification of missing knowledge, practical gaps, depth gaps, and prerequisite gaps preventing advancement toward target Backend & DevOps roles.

---

## 1. Domain-by-Domain Specific Knowledge Gaps

### 🌐 Computer Networking Infrastructure Gaps
- **Data Link & Network Layer**: ARP, Ethernet, MAC Addressing, IPv4, CIDR Subnetting (`/24`, `/16`), Routing tables (`ip route`), NAT (Network Address Translation), DHCP, ICMP (`ping`, `traceroute`).
- **Application, Security & Transport Theory**: *(RESOLVED THEORY GAP — Level 3/5)*: HTTP/1.1, HTTP/2 multiplexing, HTTP/3, TLS 1.3 Handshake, CA trust chains, ECDHE key exchange, session keys, QUIC Connection Migration. *(Remaining: WebSockets, Firewall/ACL, and packet-level captures).*
- **Diagnostics & Tools**: Wireshark packet capture analysis, `tcpdump`, `nc` (netcat), `nmap` port scanning (Target: [`P003`](../00-projects/P003-network-packet-investigation.md)).

### 🛢️ Database Internals & Backend Concurrency Gaps
- **Transactions & ACID**: `COMMIT`, `ROLLBACK`, Savepoints, Atomicity, Consistency, Isolation, Durability.
- **Concurrency Control & Locking**: Read Uncommitted, Read Committed, Repeatable Read, Serializable isolation levels, Dirty Reads, Non-Repeatable Reads, Phantom Reads, Shared/Exclusive Locks, Lock Contention, Deadlocks, Multi-Version Concurrency Control (MVCC).
- **Performance & Infrastructure**: HikariCP Connection Pooling setup, reading SQL Execution Plans (Index Seek vs Index Scan, Key Lookup cost), Index fragmentation tuning, Flyway database schema migration tools.

### ☕ Java Backend Stack Gaps
- **Build Tools**: Advanced Maven CLI usage, custom plugins, publishing artifacts, Gradle. *(Note: Core Maven project management and multi-module builds resolved via C009).*
- **Modern Java & Functional**: Advanced Stream Collectors (`Collector.of`), Parallel Streams thread safety, primitive streams (`IntStream`). *(Note: Core Lambdas, Streams filtering/mapping, and Optionals resolved via C010–C012).*
- **Automated Testing**: JUnit 5 (`@Test`, `@ParameterizedTest`), Assertions, Mockito mocking framework (`@Mock`, `when().thenReturn()`), Testcontainers.
- **Frameworks & Persistence**: Spring Boot, Spring Data JPA / Hibernate (`@Entity`, `JpaRepository`), REST API design, Spring Security & JWT, Redis caching, Kafka event streaming.



### 🐧 Linux & Systems Programming Gaps
- **Container Primitives**: Linux Network Namespaces (`ip netns`), virtual ethernet pairs (`veth`), Linux Bridge interfaces (`brctl`), `iptables` / `nftables` NAT masquerading and port forwarding.
- **Linux System Programming**: POSIX system calls (`fork`, `exec`, `wait`), `pthread` multithreading, Mutex, Semaphores, Anonymous/Named Pipes, `epoll` kernel event loops, `/proc` filesystem, `strace` system call tracing.
- **Service Operations**: Custom `systemd` `.service` unit creation, Nginx reverse proxy configuration, SSL certificate renewal.

### 🛠️ DevOps & Infrastructure Gaps
- **CI/CD Automation**: GitHub Actions workflow syntax (`.github/workflows/ci.yml`), automated Maven build/test triggers, Docker image publish actions. *(Note: GitHub Actions is CI/CD, not Git fundamentals).*
- **Containerization & Cloud**: Docker Engine, Dockerfile multi-stage builds, Docker volumes, Docker Compose (`docker-compose.yml`), AWS VPC, Terraform Infrastructure as Code, Kubernetes (K8s), Observability (Prometheus, Grafana).

### 🤖 AI Engineering & LLM Application Gaps
- **Vector Database Deployment & Indexing**: Hands-on deployment and configuration of vector databases (ChromaDB, Qdrant, Pinecone, PGVector), indexing algorithms (HNSW, IVFFlat), metadata filtering.
- **Production Framework Implementations**: Coding functional RAG pipelines using Spring AI (Java) or LangChain/LlamaIndex (Python).
- **Advanced Retrieval Techniques**: Hybrid search (BM25 keyword search + dense vector similarity), Re-ranking (Cross-Encoders), contextual compression.
- **Agentic Loops & Evaluation**: Implementing deterministic function/tool calling in multi-agent workflows, automated RAG evaluation metrics (RAGAS framework: faithfulness, answer relevancy, context precision).

---

## 2. Practical Gaps (Theory Known, Practical Missing)

```text
[Theory Learned] ------------(GAP: Practical Proof Missing)------------> [Practical Mastery]
```

1. **Java Network Sockets vs Network Packet Analysis**
   - *Theory*: Java Socket API, TCP/UDP concepts (Level 3/5).
   - *Practical*: Multi-client Chat Room & Remote Desktop Java apps (Level 3/5).
   - *Gap*: Lacking hands-on packet inspection with Wireshark/tcpdump to observe TCP 3-way handshake, retransmission timeouts, and packet loss behavior.
   - *Designated Assessment Instrument*: [`P003 — Network Packet Investigation Lab`](../00-projects/P003-network-packet-investigation.md)

2. **Database Queries & JDBC vs Concurrency & Transactions**
   - *Theory*: SQL Server queries, JOINs, CTEs, JDBC DAO pattern (Level 3/5).
   - *Practical*: SQL Server queries & JDBC DAO exercises (Level 3/5).
   - *Gap*: Zero practical experience with HikariCP connection pooling, `conn.setAutoCommit(false)` explicit transaction rollbacks, or testing isolation levels under concurrent writes.
   - *Designated Assessment Instrument*: [`P002 — Database Transaction & Concurrency Lab`](../00-projects/P002-database-concurrency-lab.md)

3. **Linux Admin vs Linux Network Namespaces**
   - *Theory*: Linux CLI, FHS, permissions, Bash scripting (Level 3/5).
   - *Practical*: Ubuntu CLI administration & Bash automation scripts (Level 3/5).
   - *Gap*: Lacking practical creation of Linux network namespaces (`ip netns`) and virtual bridges (`brctl`) required as Docker networking prerequisites.
   - *Designated Assessment Instrument*: [`P004 — Linux Process & Network Diagnostics`](../00-projects/P004-linux-diagnostics.md)

4. **Java Application Multithreading vs Concurrency Contention**
   - *Theory*: Thread lifecycle, race conditions, synchronization theory (Level 3/5).
   - *Practical*: Single thread per client socket routing (Level 3/5).
   - *Gap*: Has not demonstrated prevention of race conditions under high contention (e.g. simultaneous stock borrowing).
   - *Designated Assessment Instrument*: [`P001 — Java Multi-user Library / Book Lending Server`](../00-projects/P001-java-library-server.md)

5. **LLM & RAG Architecture vs Production Application Implementation**
   - *Theory*: LLM limitations, RAG Ingestion/Retrieval pipelines, Vector embeddings, Agentic loop (Level 3/5).
   - *Practical*: Conceptual understanding from video lectures (Level 2/5).
   - *Gap*: Has not yet written code to parse documents, generate embeddings via API, query a vector store, and generate answers in a live application.

---

## 3. Prerequisite Gap Verification for Target Pathways

> 💡 **Prerequisite Policy**: We only enforce strict dependencies required to *start* a pathway. Follow-on skills are tracked as subsequent topics, not artificial prerequisites.

### Pathway A: Spring Boot Microservices
- **Strict Prerequisites Needed to Start**:
  1. Java Core & OOP: **READY (3/5)**
  2. SQL Queries & Database: **READY (3/5)**
  3. Maven Build Tool: **READY (3/5)** -> *RESOLVED GAP (via C009)*
  4. Java 8 Streams API & Lambdas: **READY (3/5)** -> *RESOLVED GAP (via C010–C012)*
  5. Basic Testing (JUnit 5): **PARTIALLY READY (1/5)** -> *PREREQUISITE GAP (test runner covered in C009, write basic assertions)*
- **Follow-on Skills (NOT Prerequisites to start Spring Boot)**:
  - Spring Data JPA / Hibernate *(learned alongside/after Spring Boot basics)*
  - Spring Security & JWT
  - Redis & Kafka
- **Verdict**: **READY TO LAUNCH SPRING BOOT**. All primary syntax, database, build, and functional prerequisites are satisfied at Level 3/5. Write a few basic JUnit 5 assertions and you can enter Spring Boot Core.



### Pathway B: Docker Container Networking
- **Strict Prerequisites Needed to Start**:
  1. Linux CLI & SysAdmin: **READY (3/5)**
  2. Bash Scripting: **READY (3/5)**
  3. Computer Networking Fundamentals (CIDR, Routing, NAT): **NOT READY (1/5)** -> *PREREQUISITE GAP*
  4. Linux Network Namespaces & Bridges: **NOT READY (1/5)** -> *PREREQUISITE GAP*
- **Supporting Context (NOT a substitute for Networking Infra)**:
  - Java Socket Programming (Level 3/5) provides application-layer context, but does **not** replace Layer 2/3 networking primitives.
- **Verdict**: **PARTIALLY READY**. Complete CIDR Subnetting and Linux Network Namespaces before Docker Networking.

---

## 4. Assessment Project Mapping for Gap Remediation

The projects defined in [`00-projects/`](../00-projects/README.md) serve as standardized evaluation instruments to resolve the tracked gaps above:

| Tracked Knowledge / Practical Gap | Designated Assessment Instrument | Required Evidence to Resolve Gap | Target Skill Score |
| :--- | :--- | :--- | :---: |
| **Java Concurrency & Race Conditions** | [`P001: Java Library Server`](../00-projects/P001-java-library-server.md) | Synchronized simultaneous borrow scenario; automated JUnit 5 concurrency tests | Practical: **4/5** |
| **Database ACID, Locks & Isolation** | [`P002: DB Concurrency Lab`](../00-projects/P002-database-concurrency-lab.md) | Proven Dirty Read/Phantom Read reproduction & prevention scripts; deadlock graph XML | Practical: **4/5** |
| **Networking Infrastructure & CIDR** | [`P003: Packet Investigation Lab`](../00-projects/P003-network-packet-investigation.md) | `.pcapng` capture files of TCP 3-way handshake; CIDR binary subnet calculations | Practical: **3/5** |
| **Linux Process, strace & Namespaces** | [`P004: Linux Diagnostics`](../00-projects/P004-linux-diagnostics.md) | Filtered `strace` failure analysis; working `veth` cross-namespace ping log | Practical: **4/5** |
| **Git Conflict & GitHub Actions CI** | [`P005: Git & CI Assessment`](../00-projects/P005-git-ci-assessment.md) | Interactive rebase log; functional `.github/workflows/ci.yml` blocking PR on test failure | CI/CD: **3/5** |
| **Docker Bridge & iptables NAT** | [`P006: Docker Networking Lab`](../00-projects/P006-docker-networking-lab.md) | Docker-to-Linux namespace mapping; `iptables` DNAT rule analysis; custom bridge DNS proof | Practical: **4/5** |

