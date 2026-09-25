# Domain: Databases — Summary

## Current Level Assessment
- **SQL Server Querying & T-SQL**: 3/5 (Theory: 3/5, Practical: 3/5, Troubleshooting: 2/5, Design: 2/5) — *Verified via SSMS SQL exercises.*
- **Java JDBC & DAO Pattern**: 3/5 (Theory: 3/5, Practical: 3/5, Troubleshooting: 2/5, Design: 2/5) — *Verified via Java DAO Model classes.*
- **Database Internals & Advanced Concurrency**: 1/5 (Theory: 2/5, Practical: 1/5, Troubleshooting: 0/5, Design: 0/5) — *Unverified / Critical Prerequisite Gap.*

---

## What I Have Learned
- SQL Server 2022 setup, SSMS administration tool.
- Complex SQL queries (`SELECT`, `JOIN`s, `GROUP BY`, `HAVING`, `UNION`, Subqueries, CTEs, Window Functions).
- Database Schema Management (DDL: `CREATE`, `ALTER`, `DROP`) and Data Manipulation (DML: `INSERT`, `UPDATE`, `DELETE`).
- Database objects: Indexes (Clustered/Non-Clustered concepts), Views, T-SQL Stored Procedures, Triggers.
- Azure SQL Cloud deployment overview.
- Java JDBC connectivity, `DriverManager`, `Connection`, `Statement`, `PreparedStatement`.
- SQL Injection protection via parameterized queries.
- Data Access Object (DAO) architecture pattern for Java applications.

---

## Critical Missing Knowledge Gaps (Backend & System Prerequisites)

The following database topics have **NOT** yet been verified with practical evidence and represent critical prerequisites for Spring Boot, JPA/Hibernate, Redis, Kafka, and High-Concurrency System Design:

1. **Transactions & ACID Properties**:
   - `COMMIT`, `ROLLBACK`, Savepoints.
   - Atomicity, Consistency, Isolation, Durability guarantees in database engines.
2. **Transaction Isolation Levels**:
   - Read Uncommitted, Read Committed, Repeatable Read, Serializable.
   - Concurrency anomalies: Dirty Reads, Non-Repeatable Reads, Phantom Reads.
3. **Database Concurrency Control & Locking**:
   - Shared Locks (S), Exclusive Locks (X), Intent Locks.
   - Row-level vs Table-level locking, Lock Contention, Deadlocks detection & resolution.
   - Multi-Version Concurrency Control (MVCC) mechanics in modern databases.
4. **Connection Pooling**:
   - HikariCP connection pool setup, minimum idle, maximum pool size configuration in Java backend apps.
5. **Query Performance Tuning & Internals**:
   - Reading SQL Execution Plans (Index Seek vs Index Scan, Key Lookup cost, Hash Join vs Nested Loop).
   - Index Fragmentation analysis, Covering Indexes, Query Store profiling.
6. **Schema Migration & Versioning**:
   - Flyway / Liquibase database schema migration tools integrated with Java applications.

---

## Strong Areas
- Writing complex SQL queries (multi-table JOINs, aggregate functions, subqueries, CTEs, Window Functions).
- Building clean DAO layers in Java using `PreparedStatement` to interact with SQL databases.

## Weak Areas
- Database Connection Pooling (HikariCP) in Java.
- Database Transactions (`COMMIT`/`ROLLBACK`) and Isolation Level handling in code.
- ORM Frameworks (Spring Data JPA / Hibernate).
- Query Performance Tuning (Execution Plans, Index optimization, Profiling).

## Recommended Supplements
1. **Transactions & ACID**: Practice manual JDBC transaction control (`conn.setAutoCommit(false)`, `conn.commit()`, `conn.rollback()`).
2. **HikariCP Connection Pool**: Integrate HikariCP connection pool with JDBC/Java.
3. **Spring Data JPA & Hibernate**: Learn Spring Data JPA ORM mapping.
4. **Flyway Migration**: Implement Flyway database schema versioning scripts.

## Readiness for Next Topics
- **Relational Querying & JDBC DAO**: **READY (3/5)**
- **High-Concurrency Backend Persistence**: **PARTIALLY READY (2/5)**
  - SQL Querying: 3/5
  - JDBC & DAO: 3/5
  - HikariCP Connection Pool: 0/5
  - ACID & Transactions: 1/5
  - JPA / Hibernate ORM: 0/5
  - *Action*: Master Transactions, HikariCP, and JPA/Hibernate before building high-concurrency backend services.
