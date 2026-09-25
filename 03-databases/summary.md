# Domain: Databases — Summary

## Current Level
- **Overall**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## What I Have Learned
- SQL Server 2022 setup, SSMS administration tool.
- Complex SQL queries (`SELECT`, `JOIN`s, `GROUP BY`, `HAVING`, `UNION`, Subqueries, CTEs, Window Functions).
- Database Schema Management (DDL: `CREATE`, `ALTER`, `DROP`) and Data Manipulation (DML: `INSERT`, `UPDATE`, `DELETE`).
- Database objects: Indexes (Clustered/Non-Clustered), Views, T-SQL Stored Procedures, Triggers.
- Azure SQL Cloud deployment overview.
- Java JDBC connectivity, `DriverManager`, `Connection`, `Statement`, `PreparedStatement`.
- SQL Injection protection via parameterized queries.
- Data Access Object (DAO) architecture pattern for Java applications.

## Strong Areas
- Writing complex SQL queries (multi-table JOINs, aggregate functions, subqueries, CTEs, Window Functions).
- Building clean DAO layers in Java using `PreparedStatement` to interact with SQL databases.

## Weak Areas
- Database Connection Pooling (HikariCP) in Java.
- Transaction Management (`COMMIT`/`ROLLBACK`) and Isolation Levels.
- ORM Frameworks (Spring Data JPA / Hibernate).
- Database Performance Tuning (Execution Plans, Index optimization, Profiling).

## Missing Knowledge
- **Connection Pooling**: HikariCP configuration.
- **ORM / Persistence**: Spring Data JPA, Hibernate, Entity Relationships (`@OneToMany`, `@ManyToOne`).
- **Database Transactions & ACID**: Explicit transaction isolation level handling.
- **Database Migration**: Flyway / Liquibase.

## Practical Gaps
- Theory Known: Database Queries & JDBC = 3/5.
- Practical Known: SQL Server queries & JDBC DAO exercises = 3/5.
- Practical Gap: No connection pool or JPA ORM integration in a real microservice/web service.

## Depth Gaps
- Indexing: Understood index lookup concept, missing execution plan reading (Index Scan vs Index Seek, Key Lookup overhead).
- JDBC: Understood statement execution, missing connection pooling and transaction manager integration.

## Recommended Supplements
1. Learn Spring Data JPA & Hibernate ORM.
2. Master HikariCP Connection Pooling setup.
3. Learn database migration with Flyway.

## Readiness
- **Backend Persistence (Spring Boot + DB)**: **PARTIALLY READY**
  - SQL Querying: 3/5
  - JDBC & DAO: 3/5
  - HikariCP: 0/5
  - JPA / Hibernate: 0/5
  - *Action*: Learn JPA/Hibernate and Spring Data JPA to complete backend persistence stack.
