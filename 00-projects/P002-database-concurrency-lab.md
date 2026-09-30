# Assessment Instrument: P002 — Database Transaction & Concurrency Lab

## 📌 Project Overview
- **Project ID**: `P002`
- **Project Name**: Database Transaction & Concurrency Lab
- **Domain**: Databases & Concurrency Control
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Practical 4/5, Troubleshooting 4/5, Theory 4/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Create a hands-on experimental lab validating database transaction boundaries, ACID guarantees, SQL Server isolation levels, concurrent transaction anomalies, deadlock scenarios, and execution plan optimization.
- **Why this project exists**: While [`C003`](../00-sources/C003-sql-server.md) proved query design (JOINs, CTEs, Window Functions) and [`C004`](../00-sources/C004-java-jdbc.md) proved basic JDBC, the repository tracks a severe gap in **Database Internals & Concurrency** (currently Level 1/5). This lab serves as the formal instrument to prove practical mastery of transactions, isolation levels, and locking mechanisms.

---

## 📋 2. Prerequisites
- SQL Server 2022 & SSMS (Level 3/5)
- Java JDBC & Prepared Statements (Level 3/5)
- Basic Understanding of ACID Theory (Level 2/5)

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- ACID principles: Atomicity via Write-Ahead Logging (WAL), Consistency constraints, Isolation via locks/MVCC, Durability via disk flush.
- ANSI SQL Transaction Isolation Levels: `READ UNCOMMITTED`, `READ COMMITTED`, `REPEATABLE READ`, `SERIALIZABLE`, and `SNAPSHOT ISOLATION`.
- Concurrency Anomalies: Dirty Reads, Non-Repeatable Reads, Phantom Reads.
- Lock hierarchy and modes: Shared (S), Exclusive (X), Intent (IS/IX), Deadlock graph analysis.

### B. Practical Skills Assessed
- Managing explicit transaction boundaries in T-SQL and Java JDBC (`conn.setAutoCommit(false)`, `conn.commit()`, `conn.rollback()`, `Savepoint`).
- Configuring and benchmarking HikariCP connection pool settings (`maximumPoolSize`, `connectionTimeout`, `leakDetectionThreshold`).
- Generating and reading SQL Server Graphical Execution Plans (identifying Table Scan, Index Scan, Index Seek, Key Lookup cost).

### C. Troubleshooting Skills Assessed
- Diagnosing blocked sessions using `sys.dm_exec_requests` and `sys.dm_tran_locks`.
- Intentionally provoking a database **Deadlock** between two concurrent transactions and capturing the SQL Server Deadlock Graph XML.
- Resolving deadlocks via consistent object access order and indexing.

### D. Design Skills Assessed
- Designing transactional workflows that balance isolation integrity against concurrency throughput.
- Designing indexes to eliminate Key Lookups and convert Index Scans to Index Seeks.

---

## 🧪 4. Required Hands-on Experiments

Every experiment must be documented with SQL scripts, execution commands, and actual output logs:

### Experiment 1: The Dirty Read Demonstration & Prevention
- **Scenario**: Transaction A updates an account balance from $1000 to $500 but does NOT commit yet.
- **Test 1**: Transaction B reads the balance under `READ UNCOMMITTED`. Does it see $500 (Dirty Read)?
- **Test 2**: Transaction A issues `ROLLBACK`. What happens to Transaction B's calculations?
- **Test 3**: Re-run Transaction B under `READ COMMITTED`. Observe how Transaction B is blocked until Transaction A commits or rolls back.

### Experiment 2: Non-Repeatable Read vs Repeatable Read
- **Scenario**: Transaction A reads row ID #1 (balance = $1000). Transaction B updates row ID #1 to $1200 and commits.
- **Test 1**: Under `READ COMMITTED`, Transaction A reads row ID #1 again in the same transaction. Prove that the value changed mid-transaction.
- **Test 2**: Change Transaction A to `REPEATABLE READ`. Prove that Transaction B is blocked from modifying row ID #1 until Transaction A completes.

### Experiment 3: Phantom Read vs Serializable
- **Scenario**: Transaction A queries `SELECT COUNT(*) WHERE balance > 500` (returns 5). Transaction B inserts a new account with balance $800 and commits.
- **Test 1**: Under `REPEATABLE READ`, prove that Transaction A can see the newly inserted row (Phantom Read).
- **Test 2**: Under `SERIALIZABLE`, prove that range locks (Key-Range Locks) prevent Transaction B's insertion until Transaction A completes.

### Experiment 4: The Deliberate Deadlock Showdown (MANDATORY)
- **Session 1**: Updates Table `Account` (Row 1), then sleeps 5 seconds, then updates Table `Orders` (Row 1).
- **Session 2**: Updates Table `Orders` (Row 1), then sleeps 5 seconds, then updates Table `Account` (Row 1).
- **Evidence Required**:
  - Prove that SQL Server chooses one session as the Deadlock Victim (Error 1205).
  - Capture the XML Deadlock Graph or SSMS Deadlock diagram.
  - Implement the code fix (standardized acquisition order) and prove deadlock elimination.

### Experiment 5: Execution Plan & Index Optimization
- Create a table with 200,000 synthetic records.
- Run a query without an index: Capture the Execution Plan showing `Table Scan` / `Clustered Index Scan` with 100% cost.
- Create a covering Non-Clustered Index with `INCLUDE` columns.
- Re-run the query: Prove the plan converted to `Index Seek` with cost reduced by >90%.

---

## 🛑 5. Acceptance Criteria

| Criteria | Minimum Required Evidence | Advanced Proof |
| :--- | :--- | :--- |
| **ACID & Rollback** | Proven script where a mid-transaction failure triggers `ROLLBACK`, leaving zero orphan records. | Use of `Savepoint` to roll back partial transaction steps. |
| **Isolation Levels** | Concrete side-by-side logs proving Dirty Read, Non-repeatable Read, and Phantom Read behavior. | Comparative evaluation against SQL Server `READ COMMITTED SNAPSHOT` (RCSI / MVCC). |
| **Deadlock Analysis** | Captured deadlock graph XML with identification of conflicting resources and victim thread. | Automated retry logic in Java JDBC catching SQL error code 1205. |
| **Connection Pool** | Configured HikariCP in Java application with active pool monitoring logs. | Stress-tested pool saturation demonstrating connection timeout handling. |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove mastery of distributed transactions (2-Phase Commit / Sagas across microservices).
- Does **NOT** prove NoSQL database architecture (Cassandra, MongoDB).
- Does **NOT** prove Spring Data JPA annotation magic (this lab requires raw T-SQL and JDBC transaction verification).

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed lab to AI for assessment:*

```markdown
Project ID: P002
Project Name: Database Transaction & Concurrency Lab
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Lab Execution Overview
- DBMS used: [e.g., SQL Server 2022 Express / Developer]
- Client tools used: [SSMS / DBeaver / Java JDBC]

### 2. Isolation Experiments Evidence
- Dirty Read demonstrated (Yes/No + script link):
- Non-repeatable Read demonstrated (Yes/No + script link):
- Phantom Read demonstrated (Yes/No + script link):

### 3. Deadlock Evidence
- Deadlock XML / screenshot captured: [Attach snippet or file link]
- Victim resolution analysis:
- Fix implemented:

### 4. Index Optimization Evidence
- Before Index (Execution plan operator + cost):
- After Index (Execution plan operator + cost):

### 5. HikariCP Configuration
- Maximum pool size tested:
- Leak detection / timeout logs attached:
```
