# Course Summary: C004 — Lập trình Java tương tác với CSDL (JDBC)

## Course Overview
- **Course ID**: C004
- **Provider**: TITV
- **Course Name**: Lập trình Java tương tác với Cơ sở dữ liệu (JDBC)
- **URL**: [https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/)
- **Status**: Completed
- **Total Lectures**: 9 Video Lessons

## Topics Covered
1. **JDBC Architecture**: Overview of JDBC API and database drivers.
2. **SQL Review**: Basic SQL query refresher.
3. **Database Connection**: Connecting Java to databases via `DriverManager.getConnection()`.
4. **JDBC Workflow**: 5 steps to interact with SQL databases in Java.
5. **Data Access Object (DAO) Pattern**: Creating generic `DAOInterface<T>` and concrete DAO classes for Model entities.
6. **DML via JDBC**: Executing `INSERT`, `UPDATE`, `DELETE` statements.
7. **DQL via JDBC**: Querying databases using `SELECT` and mapping `ResultSet` rows to Java objects.
8. **PreparedStatement**: Parameterized SQL queries, SQL Injection prevention, query execution plan caching.
9. **Data Type Mapping**: Type mapping between JDBC Types and Java Types.

## Topics Already Known Before Course
- Basic SQL queries (from C003).
- Java OOP class structure (from C001).

## New Knowledge Added
- JDBC Driver Manager, Connection, Statement, PreparedStatement, ResultSet interfaces.
- SQL Injection vulnerabilities and prevention via parameterized queries.
- Data Access Object (DAO) design pattern architecture.

## Knowledge Deepened
- Mapping relational table columns to Java model object properties.

## Practical Skills Added
- Connecting Java applications to SQL Server / MySQL databases.
- Implementing DAO classes for domain models (`SachDAO`, `KhachHangDAO`).
- Writing secure queries with `PreparedStatement`.

## Remaining Gaps
- Connection Pooling (HikariCP).
- Explicit Transaction Management (`commit`/`rollback`).
- Object-Relational Mapping (Spring Data JPA / Hibernate).

## Knowledge Not Covered
- ORM Frameworks (Spring Data JPA, Hibernate).
- HikariCP connection pool setup.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
1. Learn Connection Pooling with HikariCP.
2. Master Spring Data JPA and Hibernate.

## Lecture Index & Direct Lesson Links

Main Course Page: [https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/)

| # | Lecture / Lesson Title | Direct Lesson URL |
| :---: | :--- | :--- |
| 1 | JDBC 01. Giới thiệu khóa học lập trình Java tương tác với Cơ sở dữ liệu Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50313) |
| 2 | JDBC 02. Ôn tập câu lệnh SQL Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50314) |
| 3 | JDBC 03. Cách kết nối với cơ sở dữ liệu bằng JDBC Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50315) |
| 4 | JDBC 04. Các bước sử dụng JDBC để tương tác Cơ sở dữ liệu Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50316) |
| 5 | JDBC 05. Xây dựng các lớp Data Access Object cho các lớp model Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50317) |
| 6 | JDBC 06. Sử dụng JDBC để thêm, xóa, cập nhật dữ liệu bằng câu lệnh INSERT, UPDATE, DELETE Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50318) |
| 7 | JDBC 07. Sử dụng JDBC để truy vấn cơ sở dữ liệu với câu lệnh SELECT Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50319) |
| 8 | JDBC 08. Nên sử dụng PreparedStatement thay thế cho Statement khi dùng JDBC để tương tác CSDL Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50320) |
| 9 | JDBC 09. Ánh xạ kiểu dữ liệu giữa JDBC Type và Java Type Video lesson | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/50321) |
| 10 | [Video] Thị giác máy tính - Computer ... | [Watch Lesson](https://titv.vn/courses-page/video-thi-giac-may-tinh-computer-vision) |
| 11 | Cấu trúc dữ liệu và giải thuật Java | [Watch Lesson](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java) |
| 12 | [Video] Nguyên lý Hệ điều hành | [Watch Lesson](https://titv.vn/courses-page/he-dieu-hanh) |
| 13 | [Video] SQL Server - Cơ bản và Nâng cao | [Watch Lesson](https://titv.vn/courses-page/sql-server) |
| 14 | [Video] Lập trình mạng (sử dụng Java) | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java) |

