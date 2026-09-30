# Technical Assessment Rubric & Evidence Criteria

This document defines the strict, objective standards by which the AI Knowledge Base Maintainer evaluates project submissions, verifies evidence, and calculates skill score adjustments.

---

## 📐 1. Multidimensional 0–5 Evaluation Scale

Every subskill is evaluated independently across five dimensions. A score increase in one dimension does not automatically increase other dimensions.

```text
Level 0: Not Learned (No exposure, no evidence)
Level 1: Terminology Known (Recognizes keywords; cannot explain mechanisms or code independently)
Level 2: Concept Understood (Explains basic conceptual purpose; cannot explain internal mechanisms)
Level 3: Mechanism Understood (Explains HOW and WHY; implements standard use cases; handles routine tasks)
Level 4: Able to Implement & Validate (Independently builds resilient systems, tests failure modes, configures environments)
Level 5: Troubleshoot & System Design (Diagnoses deep production anomalies, analyzes complex trade-offs, architectures solutions)
```

### Detailed Dimensional Breakdown

| Dimension | Level 2 Requirement | Level 3 Requirement | Level 4 Requirement | Level 5 Requirement |
| :--- | :--- | :--- | :--- | :--- |
| **Theory** | Can describe what a technology does and why it exists. | Can detail the internal data structures, algorithms, lifecycle, and communication protocols. | Explains trade-offs between competing designs, internals, and edge cases. | Formulates theoretical proofs, mathematical intuitions, or formal specification analysis. |
| **Practical** | Runs sample code or basic scripts with guidance. | Implements working features, builds clean interfaces, and writes basic unit tests. | Implements complete end-to-end architectures, handles concurrency, configures build tools, and writes comprehensive automated test suites. | Optimizes low-level performance, implements custom protocol engines or framework internals. |
| **Troubleshooting** | Identifies obvious syntax errors and reads simple stack traces. | Diagnoses common runtime exceptions (NPE, ClassNotFound, SQL syntax) using print statements or simple debugger. | Reproduces race conditions, memory leaks, connection leaks, or network drops using profilers, thread dumps, `strace`, or Wireshark. | Solves complex intermittent production deadlocks, packet reordering, kernel contention, or corrupted state. |
| **Design** | Replicates boilerplate design patterns without modifying structure. | Decouples components cleanly (e.g. MVC, DAO, service layers) and models domain entities. | Designs modular systems that tolerate failures, isolates state, applies appropriate concurrency guards, and optimizes data models. | Architects high-availability, distributed, horizontally scalable, fault-tolerant enterprise topologies. |

---

## 🔬 2. Evidence Quality Standards

Evidence status determines whether a skill rating can be updated:

| Evidence Status | Definition | Impact on Skill Matrix |
| :--- | :--- | :--- |
| **`Verified`** | Proven by functional source code, passing automated tests, Git commit logs, or diagnostic captures (`.pcapng`, `strace`, thread dump). | Can support score increase up to Level 4/5 or Level 5/5. |
| **`Partial`** | Concept is demonstrated in code, but automated tests, concurrency handling, or failure scenarios are absent. | Maximum allowable score is Level 3/5. |
| **`Not Verified`** | Feature or capability is claimed in documentation/README or submission text, but code/evidence cannot be found, accessed, or executed. | **No score change permitted**. Status flagged as unverified. |
| **`No Evidence`** | Capability has never been submitted or demonstrated. | Score remains at Level 0/5 or 1/5. |

---

## 🛡️ 3. Domain Evidence Verification Matrices

### A. Java Core & Concurrency
- **To Achieve Practical 3/5**: Working classes, OOP inheritance/composition, Collections (`Map`, `List`, `Set`), File I/O, Maven build configuration.
- **To Achieve Practical 4/5**: Thread pool management (`ExecutorService`), thread synchronization (`ReentrantLock`, `synchronized`, `AtomicInteger`), prevention of race conditions, robust error handling, automated JUnit 5 tests.
- **To Achieve Troubleshooting 3/5**: Demonstrates reproduction and resolution of a concurrency bug (e.g. data corruption from race condition) using logs, unit tests, or thread inspection.
- **Boundary**: Concurrency in memory does **not** prove database transaction isolation.

### B. Database & Persistence
- **To Achieve Practical 3/5**: Complex `SELECT`, `JOIN`, subqueries, CTEs, Window functions, JDBC `PreparedStatement`, DAO pattern.
- **To Achieve Practical 4/5**: Explicit transaction boundaries (`conn.setAutoCommit(false)`, `commit()`, `rollback()`), savepoints, HikariCP connection pool configuration, index usage.
- **To Achieve Troubleshooting 3/5**: Analyzing SQL execution plans (Index Scan vs Index Seek), reproducing and resolving a deadlock or dirty read under concurrent transactions.
- **Boundary**: Query syntax mastery does **not** prove transaction isolation or database internals.

### C. Networking & Communications
- **To Achieve Practical 3/5 (Java Socket)**: Functional client-server communication using `Socket` and `ServerSocket`, multithreaded client handlers, binary/text protocol parsing.
- **To Achieve Practical 3/5 (Computer Networking)**: Configuring IP routing, CIDR subnetting calculations, inspecting ARP tables, testing ICMP/DNS resolution.
- **To Achieve Troubleshooting 3/5 (Computer Networking)**: Wireshark or `tcpdump` packet capture analyzing TCP 3-way handshake (`SYN`, `SYN-ACK`, `ACK`), connection termination (`FIN`/`RST`), or packet retransmission.
- **Boundary**: Writing a Java Socket chat application does **not** prove Computer Networking Infrastructure capability.

### D. Operating Systems & Linux
- **To Achieve Practical 3/5**: Linux CLI administration, FHS navigation, user/group permission management (`chmod`, `chown`), Bash automation scripting.
- **To Achieve Practical 4/5**: System service management (`systemd` unit files), process monitoring (`/proc`, `ps`, `top`, `kill` signals), network socket inspection (`ss`, `netstat`).
- **To Achieve Troubleshooting 3/5**: Tracing process system calls using `strace`, analyzing file descriptor leaks (`lsof`).
- **To Achieve Advanced Systems / Container Primitives (4/5)**: Manual creation of isolated network namespaces (`ip netns`), virtual ethernet pairs (`veth`), and bridge interfaces (`brctl` / `ip link`).
- **Boundary**: Basic shell commands do **not** prove OS kernel concepts or container network internals.

### E. Git & DevOps
- **To Achieve Practical 4/5 (Git Version Control)**: Branching, merging, rebasing onto upstream, conflict resolution, atomic commits, Git tag/release creation.
- **To Achieve Practical 3/5 (CI/CD)**: Creating functional GitHub Actions workflow files (`.github/workflows/*.yml`) that automatically checkout, build with Maven, and run tests on push/PR.
- **Boundary**: Git CLI mastery does **not** equal CI/CD workflow mastery. They are evaluated separately.

---

## 🔄 4. Score Adjustment Protocol

When an assessment report recommends updating a skill score, the AI Maintainer must record:
1. **Skill Name**
2. **Dimension** (Theory / Practical / Troubleshooting / Design / Confidence)
3. **Before Score**
4. **After Score**
5. **Concrete Evidence Reference** (Project ID, file path, commit hash)
6. **Technical Rationale** (Why this evidence proves the transition to the new level)

```markdown
Example Record:
- Skill: Java Concurrency & Multithreading
- Dimension: Practical
- Transition: 2/5 -> 4/5
- Evidence: P001 (commit 8f3b12a, `src/main/java/server/BookService.java:L45-L78`)
- Rationale: Demonstrated synchronized critical sections preventing over-borrowing under 10 concurrent threads with automated JUnit 5 tests.
```
