# Java Database Connectivity (JDBC) & DAO Pattern

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: High

## What I Have Learned
- **JDBC Core Architecture**:
  - JDBC API architecture, JDBC Driver Manager, loading SQL database drivers (`Class.forName("...")` or ServiceLoader).
  - Establishing database connections (`Connection conn = DriverManager.getConnection(url, user, pass)`).
- **Executing Statements & CRUD Operations**:
  - `Statement` interface for static SQL execution (`executeUpdate()`, `executeQuery()`).
  - `ResultSet` processing (`rs.next()`, `rs.getString()`, `rs.getInt()`, `rs.getTimestamp()`).
  - DML execution via JDBC: `INSERT`, `UPDATE`, `DELETE`.
  - DQL execution via JDBC: `SELECT` queries mapped to Java Model objects.
- **PreparedStatement & Security**:
  - `PreparedStatement` interface with parameterized placeholders (`?`).
  - Parameter binding (`pstmt.setString(1, val)`, `pstmt.setInt(2, val)`).
  - Prevention of **SQL Injection** security vulnerabilities.
  - Performance advantage of pre-compiled execution plans in database engines.
- **Data Access Object (DAO) Pattern**:
  - Decoupling database interaction logic from business logic.
  - Creating `DAOInterface<T>` generic interface (`insert()`, `update()`, `delete()`, `selectAll()`, `selectById()`, `selectByCondition()`).
  - Implementing concrete DAO classes for model entities (e.g., `KhachHangDAO`, `SanPhamDAO`, `SachDAO`).
- **Data Type Mapping**:
  - Mapping SQL data types (`VARCHAR`, `INT`, `DOUBLE`, `DATE`, `TIMESTAMP`) to Java data types (`String`, `int`, `double`, `java.sql.Date`, `java.sql.Timestamp`).

## What I Understand
- Why `PreparedStatement` MUST be used over `Statement` to avoid SQL injection attacks and benefit from query plan caching.
- Architecture of the Data Access Object (DAO) pattern in maintaining clean separation of concerns.
- Resource lifecycle management in JDBC (`Connection`, `Statement`, `ResultSet` closing resources to prevent database connection leaks).
- Data type transformation between Java JVM memory representation and SQL relational database columns.

## What I Can Do
- Connect Java applications to relational databases (SQL Server, MySQL) using JDBC drivers.
- Implement DAO classes for CRUD operations on domain models.
- Write secure SQL queries with parameterized `PreparedStatement`.
- Map database `ResultSet` rows into Java object graphs.

## What I Cannot Yet Do
- Use Connection Pooling libraries (HikariCP, Apache DBCP) for high-concurrency database connection management.
- Manage multi-operation Database Transactions (`Connection.setAutoCommit(false)`, `commit()`, `rollback()`, Savepoints).
- Use modern Java ORM / Persistence Frameworks (Hibernate, Spring Data JPA, MyBatis).
- Handle N+1 query problems in object-relational mapping manually.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-004** — Lập trình Java tương tác với Cơ sở dữ liệu (JDBC) (TITV) | URL: https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/ | Lessons 01-09 (Connection, PreparedStatement, DAO Pattern)
- **SRC-003** — SQL Server (TITV) | URL: https://titv.vn/courses-page/sql-server/ | Relational query foundation

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Manual JDBC connection handling without Connection Pool (HikariCP).
- Lack of explicit Transaction Management (`commit`/`rollback`) handling in multi-step business operations.
- No experience with JPA/Hibernate ORM framework.

## Missing Knowledge
- Connection Pooling: HikariCP setup and pool sizing.
- JDBC Transactions & Isolation levels in Java code.
- JPA / Hibernate ORM Framework (`@Entity`, `@Table`, `@Id`, `@OneToMany`, `@ManyToOne`).

## Recommended Supplement
1. Learn Connection Pooling with HikariCP.
2. Implement explicit transaction management with `Connection.setAutoCommit(false)` in JDBC.
3. Transition from raw JDBC to JPA / Spring Data JPA.
