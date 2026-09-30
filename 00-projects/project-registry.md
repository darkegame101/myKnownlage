# Master Assessment Project Registry

Canonical registry of all practical assessment projects, diagnostic labs, and historical evidence records.

---

## 🎯 1. Active & Planned Assessment Instruments (`P001` – `P006`)

These assessment projects are designed as rigorous testing instruments to evaluate practical skills, failure scenarios, concurrency handling, and system diagnostics.

| Project ID | Project Name | Purpose / Core Objective | Domain | Primary Skills Assessed | Prerequisites | Status | Evidence Status | Repository | Assessment Date | Target / Current Score | Instrument Link |
| :--- | :--- | :--- | :--- | :--- | :--- | :---: | :---: | :--- | :---: | :---: | :---: |
| **P001** | Java Multi-user Library / Book Lending Server | Evaluate multi-client concurrency, race conditions, DAO pattern, and TCP client-server architecture under high contention | Programming / Databases / Networking | Java Core, OOP, Collections, Maven, JDBC, SQL, TCP Sockets, Multithreading, Concurrency, Testing | Java Core (3/5), SQL (3/5), Sockets (3/5) | Planned | No Evidence | TBD | Pending | Target: Practical 4/5 | [`P001`](./P001-java-library-server.md) |
| **P002** | Database Transaction & Concurrency Lab | Evaluate ACID properties, isolation levels (Dirty/Phantom reads), explicit locks, deadlocks, and connection pooling | Databases | SQL Server, ACID, Isolation Levels, Deadlocks, MVCC, Execution Plans, HikariCP | SQL Queries (3/5), JDBC (3/5) | Planned | No Evidence | TBD | Pending | Target: Practical 4/5 | [`P002`](./P002-database-concurrency-lab.md) |
| **P003** | Network Packet Investigation Lab | Evaluate packet-level diagnostic abilities, protocol analysis, TCP 3-way handshake, ARP, DNS, TLS, and packet drops | Networking | CIDR Subnetting, ARP, IP Routing, ICMP, TCP Handshake, UDP, DNS, Wireshark, tcpdump | OS Concepts (3/5), Linux CLI (3/5) | Planned | No Evidence | TBD | Pending | Target: Practical 3/5 | [`P003`](./P003-network-packet-investigation.md) |
| **P004** | Linux Process & Network Diagnostics | Evaluate OS process monitoring, signals, `/proc` filesystem inspection, systemd unit configuration, `strace`, and network namespaces | Operating Systems | Linux CLI, Process PID, Signals, `/proc`, `systemd`, `strace`, Network Namespaces, `veth` | Linux CLI (3/5), Bash (3/5) | Planned | No Evidence | TBD | Pending | Target: Practical 4/5 | [`P004`](./P004-linux-diagnostics.md) |
| **P005** | Git Engineering Workflow + CI | Evaluate professional Git workflows (branching, interactive rebasing, merge conflict resolution, PRs) and automated GitHub Actions CI pipelines | DevOps Tools | Git CLI, Branching, Rebase, Cherry-pick, Conflict Resolution, GitHub Actions CI/CD | Git CLI (4/5), Maven (3/5) | Planned | No Evidence | TBD | Pending | Target: Practical 4/5 | [`P005`](./P005-git-ci-assessment.md) |
| **P006** | Docker Networking Lab | Evaluate container networking from Linux primitives (network namespaces, `veth` pairs, bridge interfaces, iptables NAT) up to Docker bridge and port publishing | Operating Systems / DevOps Tools | Linux Network Namespaces, Virtual Bridges, `iptables` NAT, Docker Networking, Port Mapping | P003, P004, Docker Basics | Planned | No Evidence | TBD | Pending | Target: Practical 4/5 | [`P006`](./P006-docker-networking-lab.md) |

---

## 🏛️ 2. Historical Evidence Registry (`P-HIST-001` – `P-HIST-005`)

These records represent practical exercises and projects completed in earlier learning sources (`C001` – `C009`). They establish our existing baseline scores and explicitly document what was proven and what was **NOT** proven.

> ⚠️ **Strict Constraint**: Historical projects maintain their existing baseline ratings. They cannot be used to inflate scores beyond what was originally verified in course work.

| Project ID | Project Name | Underlying Course | Domain | Skills Proven | Explicit Limitations (What is NOT Proven) | Status | Evidence Status | Assessment Date | Current Score |
| :--- | :--- | :--- | :--- | :--- | :--- | :---: | :---: | :---: | :---: |
| **P-HIST-001** | Java Multithreaded Chat Room Application | [`C006`](../00-sources/C006-java-network.md) | Networking | `ServerSocket`, `Socket`, TCP Client/Server threads, basic message routing | Does NOT prove packet inspection, Wireshark, CIDR, TLS, or connection pooling | Completed | Verified | 2026-09-30 | Practical: 3/5 |
| **P-HIST-002** | Java Remote Desktop Control Application | [`C006`](../00-sources/C006-java-network.md) | Networking / Programming | `java.awt.Robot`, UDP Datagrams, screen capture streaming, remote input events | Does NOT prove low-latency streaming optimization or network layer routing | Completed | Verified | 2026-09-30 | Practical: 3/5 |
| **P-HIST-003** | Custom Singly Linked List Student Manager | [`C002`](../00-sources/C002-dsa-java.md) | DSA / Programming | Node manipulation, pointer traversal, insertion, deletion, console UI | Does NOT prove Doubly Linked Lists, Trees, Graphs, or algorithmic optimization | Completed | Verified | 2026-09-30 | Practical: 2/5 |
| **P-HIST-004** | Linux Server Administration & Bash Automation Suite | [`C008`](../00-sources/C008-linux-bash.md) | Operating Systems | Ubuntu CLI, user/group permission configuration, Bash automation loops, file checks | Does NOT prove system programming (`fork`/`exec`), `strace`, or network namespaces | Completed | Verified | 2026-09-30 | Practical: 3/5 |
| **P-HIST-005** | Maven Multi-Module Build & Testing Setup | [`C009`](../00-sources/C009-maven-java.md) | Programming | `pom.xml`, dependency inheritance, multi-module packaging (WAR/JAR), Maven test runner | Does NOT prove custom Maven plugin authoring or Mockito integration test suites | Completed | Verified | 2026-09-30 | Practical: 3/5 |

---

## 📈 3. Project Status Lifecycle Definitions

- **`Planned`**: Assessment instrument specifications and acceptance criteria are defined; development not yet initiated.
- **`In Progress`**: User is actively implementing the codebase or diagnostic lab.
- **`Completed`**: User has implemented the required features and prepared a submission.
- **`Verified`**: AI Knowledge Base Maintainer has reviewed the repository code, verified tests/logs, and updated all dashboards.
