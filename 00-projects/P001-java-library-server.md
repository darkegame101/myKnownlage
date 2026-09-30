# Assessment Instrument: P001 — Java Multi-user Library / Book Lending Server

## 📌 Project Overview
- **Project ID**: `P001`
- **Project Name**: Java Multi-user Library / Book Lending Server
- **Domain**: Java Programming / Databases / Sockets / Concurrency
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Practical 4/5, Troubleshooting 3/5, Design 3/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Build a multi-client TCP server that manages a library book catalog and loan processing, backed by SQL Server via JDBC and DAO pattern, supporting concurrent client connections and thread-safe inventory borrowing.
- **Why this project exists**: While previous exercises proved basic Java Sockets ([`P-HIST-001`](./project-log.md#entry-p-hist-001--java-multithreaded-chat-room-application)) and SQL queries ([`C003`](../00-sources/C003-sql-server.md)), this project is the primary instrument to assess whether the student can integrate networking, multithreading, concurrency guards, and database persistence into a coherent, thread-safe backend architecture.

---

## 📋 2. Prerequisites
- Java Core Syntax & OOP (Level 3/5)
- Java Collections Framework (Level 3/5)
- Apache Maven Build Management (Level 3/5)
- SQL Server Querying & JDBC DAO (Level 3/5)
- Java Socket API (Level 3/5)

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- TCP client-server lifecycle (`ServerSocket`, `Socket`, TCP connection teardown).
- Java memory model and concurrency concepts (race conditions, critical sections, atomicity).
- Layered backend architecture: Transport $\rightarrow$ Controller/Handler $\rightarrow$ Service $\rightarrow$ DAO $\rightarrow$ SQL Database.

### B. Practical Skills Assessed
- Configuring a Maven multi-module or clean standard project (`pom.xml`).
- Implementing `ExecutorService` thread pool to handle concurrent TCP client sessions.
- Implementing DAO layer using JDBC `PreparedStatement` to prevent SQL Injection.
- Applying synchronization primitives (`synchronized`, `ReentrantLock`, or Atomic variables) to prevent double-booking.

### C. Troubleshooting Skills Assessed
- Reproducing race conditions under load and diagnosing state corruption.
- Analyzing thread dumps to identify thread starvation or deadlocks.
- Handling unexpected client disconnects cleanly without server crashes or socket leaks.

### D. Design Skills Assessed
- Separation of concerns: Network communication protocol decoupled from core business domain logic.
- Clean DAO interface abstractions (`BookDao`, `BorrowDao`).
- Thread-safe shared state management.

---

## 🏗️ 4. Architecture & Technical Requirements

```text
[TCP Clients (CLI/Console)] 
       ↓ (Raw TCP / JSON / Protocol Strings)
[ServerSocket Listener] 
       ↓ (ExecutorService ThreadPool)
[ClientSessionHandler] 
       ↓
[BookLendingService]  <--- Thread-Safe Concurrency Guard (Atomic / Lock)
       ↓
[BookDao / UserDao] 
       ↓ (JDBC PreparedStatement)
[SQL Server 2022 Database]
```

### Required Features
1. **Catalog Browsing**: List all books, filter by title/author/genre with live available copy counts.
2. **Borrowing Engine**: User initiates borrow request for a specific Book ID.
3. **Return Engine**: User returns a borrowed book, restoring available stock.
4. **User Session Authentication**: Basic login/token identification over TCP socket.

### Required Failure Scenarios & Concurrency Experiment (MANDATORY)
- **The Simultaneous Borrowing Race Condition Scenario**:
  - Initial State: Book ID #101 has exactly **1 copy remaining** (`available_copies = 1`).
  - Action: Two independent TCP clients (User A and User B) submit a borrow request for Book ID #101 **at the exact same millisecond**.
  - **Failure Mode to Reproduce**: Without synchronization, both threads read `available_copies == 1`, both proceed to borrow, resulting in `available_copies == -1` (oversold inventory / data corruption).
  - **Resolution to Prove**: Implement thread synchronization or transactional lock so exactly one user receives success (`200 Borrowed`) and the second user receives an immediate clean rejection (`409 Out of Stock`).

### Required Tests (Automated)
1. **Unit Tests (JUnit 5)**: Test service logic and catalog validations in isolation.
2. **Concurrency Integration Test**: Spawn 10 concurrent threads in a test harness attempting to borrow 5 available copies. Assert that exactly 5 succeed, exactly 5 fail, and remaining stock equals 0.

### Required Debugging & Diagnostic Evidence
- Thread dump snippet or debug log demonstrating thread names handling concurrent requests.
- Log output proving the graceful handling of sudden client socket disconnects (`SocketException: Connection reset`).

### Required Git & Engineering Evidence
- Conventional commit history (`feat:`, `fix:`, `test:`, `refactor:`).
- At least one dedicated branch with a pull request demonstrating code review.

---

## 🛑 5. Acceptance Criteria

| Category | Minimum Acceptance Criteria (Verified) | Advanced Criteria (Optional Bonus) |
| :--- | :--- | :--- |
| **Networking** | Multithreaded TCP server accepting multiple concurrent clients via thread pool. | Protocol framing with length-prefix or JSON serialization. |
| **Concurrency** | Race condition resolved; zero negative stock under 10+ concurrent requests. | Non-blocking data structures or optimistic locking. |
| **Database** | JDBC DAO with `PreparedStatement` and SQL Server connectivity. | Connection pooling via HikariCP + explicit transaction rollback. |
| **Testing** | Automated JUnit 5 test reproducing and validating concurrency safety. | Stress testing with simulated 50 concurrent socket clients. |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove mastery of Layer 2/3 Computer Networking (Ethernet, CIDR, ARP, NAT, Wireshark).
- Does **NOT** prove mastery of Database Transaction Isolation levels (Dirty Read, Phantom Read, MVCC) unless explicitly configured in JDBC transactions.
- Does **NOT** prove Spring Framework mastery (this is pure Java Core / JDBC / Sockets).
- Does **NOT** prove CI/CD pipeline automation (unless paired with `P005`).

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed repository to AI for assessment:*

```markdown
Project ID: P001
Project Name: Java Multi-user Library / Book Lending Server
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Implementation Overview
- What I implemented:
- Thread pool configuration used:
- Concurrency guard mechanism implemented:
- JDBC DAO design:

### 2. Concurrency Race Condition Proof
- How the simultaneous borrow scenario was tested:
- Test results (attach console log or test pass count):

### 3. Debugging & Troubleshooting
- Bugs encountered during socket communication:
- How client disconnection was handled:
- Thread dump or diagnostic logs attached:

### 4. Known Limitations
- What is not yet supported:
- What I am still unsure about:
```
