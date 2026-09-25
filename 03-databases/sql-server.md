# SQL Server & Relational Database Management

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: High

## What I Have Learned
- **Environment & Setup**: Installing SQL Server 2022, SSMS (SQL Server Management Studio), connecting to local databases.
- **SQL Querying (DML & DQL)**:
  - Basic Queries: `SELECT`, `SELECT DISTINCT`, `SELECT TOP`, Aliases (`AS`).
  - Filtering & Sorting: `WHERE`, `ORDER BY` (ASC/DESC), `AND`, `OR`, `NOT`, `BETWEEN`, `LIKE` with Wildcards (`%`, `_`, `[]`), `IN`, `IS NULL`, `IS NOT NULL`.
  - Aggregations & Grouping: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`, `GROUP BY`, `HAVING`.
  - Date Functions: `DAY()`, `MONTH()`, `YEAR()`.
  - Joins & Unions: `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`, multi-table queries, `UNION` / `UNION ALL`.
  - Subqueries: Scalar subqueries, correlated subqueries, nested queries (`IN`, `EXISTS`).
  - Advanced Querying: Query Execution Order, CTE (Common Table Expression), Recursive CTE, Window Functions (`ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`, `OVER (PARTITION BY ... ORDER BY ...)`).
- **Database Schema & Data Modification (DDL & DML)**:
  - Database Management: `CREATE DATABASE`, `DROP DATABASE`.
  - Table Management: `CREATE TABLE`, `ALTER TABLE`, `DROP TABLE`, Data types (`INT`, `VARCHAR`, `NVARCHAR`, `DATETIME`, `DECIMAL`, `BIT`).
  - Data Modification: `INSERT INTO`, `SELECT INTO` (backup/copy tables), `UPDATE`, `DELETE`, `TRUNCATE`.
- **Database Objects & T-SQL Programming**:
  - Indexes: Concept of Indexing for performance tuning (Clustered vs Non-Clustered index).
  - Views: `CREATE VIEW`, benefits of virtual tables.
  - T-SQL & Stored Procedures: `CREATE PROCEDURE`, input/output parameters, procedure execution (`EXEC`).
  - Triggers: `CREATE TRIGGER`, `AFTER` / `INSTEAD OF` triggers, `inserted` / `deleted` pseudo-tables.
  - Azure SQL: Overview of deploying SQL Server databases to Microsoft Azure Cloud.

## What I Understand
- Relational algebra concepts behind multi-table joins (Cartesian product filtering vs hash/nested loop join strategies).
- Query execution precedence: `FROM` -> `ON` -> `JOIN` -> `WHERE` -> `GROUP BY` -> `HAVING` -> `SELECT` -> `DISTINCT` -> `ORDER BY` -> `TOP`.
- The difference between `WHERE` (filters raw rows before aggregation) and `HAVING` (filters aggregated groups).
- Common Table Expressions (CTE) vs Subqueries for query readability and recursive hierarchical queries.
- Index lookup mechanisms and why indexes accelerate `SELECT` while adding overhead to `INSERT`/`UPDATE`/`DELETE`.
- Stored Procedures and Triggers for encapsulating business logic inside database engines.

## What I Can Do
- Install and configure SQL Server 2022 and SSMS locally.
- Design relational tables with data types, primary keys, and foreign keys.
- Write complex SQL queries involving multi-table JOINs, subqueries, CTEs, and Window Functions.
- Write T-SQL Stored Procedures and Triggers for database automation.
- Perform DML operations (`INSERT`, `UPDATE`, `DELETE`, `SELECT INTO`).

## What I Cannot Yet Do
- Perform advanced Query Performance Tuning using Execution Plans, Index Fragmentation analysis, and Query Store.
- Design database high-availability (HA) and disaster recovery (DR) solutions (Always On Availability Groups, Log Shipping, Replication).
- Perform database administration tasks: backup strategies, transaction log truncation, security role auditing.
- Handle database migration scripts and schema version control tools (Flyway, Liquibase).

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-003** — SQL Server (Cơ bản và Nâng cao) (TITV) | URL: https://titv.vn/courses-page/sql-server/ | Lessons 01-47 (DQL, DDL, DML, CTE, Window Func, T-SQL)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Limited experience with database performance profiling under high concurrent write loads.
- No exposure to PostgreSQL or MySQL syntax nuances (studied SQL Server T-SQL specifically).
- Lack of experience with schema migration tools (Flyway/Liquibase).

## Missing Knowledge
- Database Normalization forms (1NF, 2NF, 3NF, BCNF) formal practice.
- Transaction Isolation Levels (Read Uncommitted, Read Committed, Repeatable Read, Serializable) & ACID deep dive.
- Schema Migration management (Flyway / Liquibase).

## Recommended Supplement
1. Study ACID properties and Database Transaction Isolation levels.
2. Practice database normalization (1NF -> 3NF) on complex domain schemas.
3. Learn database migration tools (Flyway) integrated with Java/Spring Boot.
