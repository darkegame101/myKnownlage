# Course Summary: C003 — SQL Server (Cơ bản và Nâng cao)

## Course Overview
- **Course ID**: C003
- **Provider**: TITV
- **Course Name**: SQL Server (Cơ bản và Nâng cao)
- **URL**: [https://titv.vn/courses-page/sql-server/](https://titv.vn/courses-page/sql-server/)
- **Status**: Completed
- **Total Lectures**: 47 Video Lessons

## Topics Covered
1. **Installation & Setup**: Installing SQL Server 2022 and SSMS, preparing sample database.
2. **Basic DQL Querying**: `SELECT`, `SELECT DISTINCT`, `SELECT TOP`, Aliases (`AS`), `MIN`, `MAX`, `COUNT`, `SUM`, `AVG`, `ORDER BY`, Arithmetic operators.
3. **Filtering & Aggregations**: `WHERE`, `AND`, `OR`, `NOT`, `BETWEEN`, `LIKE`, Wildcards (`%`, `_`), `IN`, `IS NULL`, `GROUP BY`, Date functions (`DAY`, `MONTH`, `YEAR`), `HAVING`.
4. **Multi-table Queries & Joins**: Multi-table querying, `UNION`, `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`.
5. **Subqueries & Advanced SQL**: Subqueries (Nested queries), Query Execution Order, CTE (Common Table Expression), Recursive CTE, Window Functions (`ROW_NUMBER`, `RANK`, `DENSE_RANK`).
6. **DDL & DML Operations**: Classification of SQL command groups, `CREATE DATABASE`, `CREATE/ALTER/DROP TABLE`, Data types, `INSERT INTO`, `SELECT INTO`, `DELETE`, `UPDATE`.
7. **Database Objects & T-SQL**: Indexing concepts (Clustered/Non-clustered), Views, T-SQL intro, Stored Procedures, Triggers, Microsoft Azure SQL deployment overview.

## Topics Already Known Before Course
- Basic database concept overview.

## New Knowledge Added
- SQL Server 2022 and SSMS administration.
- Advanced SQL querying: JOINs, Subqueries, CTEs, Window Functions.
- Database Schema definition (DDL) and Data manipulation (DML).
- Indexes, Views, T-SQL Stored Procedures, and Triggers.

## Knowledge Deepened
- Relational query logic, aggregation, and filtering precedence.

## Practical Skills Added
- Writing multi-table SQL queries, CTEs, and Window Functions.
- Writing T-SQL Stored Procedures and Triggers.
- Managing SQL Server databases locally via SSMS.

## Remaining Gaps
- Execution plan analysis, Index fragmentation tuning, Query Store profiling.
- Database High Availability (HA) and Disaster Recovery (DR).
- Database Schema Migration tools (Flyway / Liquibase).

## Knowledge Not Covered
- PostgreSQL / MySQL dialect differences.
- ACID deep dive & Transaction Isolation Levels.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
1. Study ACID properties and Database Transaction Isolation levels.
2. Learn Flyway database migration tool.

## Lecture Index & Direct Lesson Links

Main Course Page: [https://titv.vn/courses-page/sql-server/](https://titv.vn/courses-page/sql-server/)

| # | Lecture / Lesson Title | Direct Lesson URL |
| :---: | :--- | :--- |
| 1 | Bài 01. Hướng dẫn cài đặt SQL Server 2022 06:47 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51703) |
| 2 | Bài 02. Hướng dẫn cài đặt SSMS SQL Server Management System 06:42 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51705) |
| 3 | Bài 03. Chuẩn bị cơ sở dữ liệu để thực hành câu lệnh SQL 22:00 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51709) |
| 4 | Bài 04. Câu lệnh truy vấn SELECT 22:00 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51712) |
| 5 | Bài 05. Câu lệnh truy vấn SELECT DISTINCT lấy dữ liệu không trùng lặp 14:35 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51714) |
| 6 | Bài 06. Câu lệnh truy vấn SELECT TOP giới hạn dòng trả về 13:04 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51717) |
| 7 | Bài 07. Cách đặt tên thay thế cho cột và bảng - Alias 20:20 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51719) |
| 8 | Bài 08. Tìm giá trị Min và Max trong SQL 17:14 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51721) |
| 9 | Bài 09. Các hàm COUNT, SUM và AVG trong SQL 23:45 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51723) |
| 10 | Bài 10. Order By - Sắp xếp kết quả trả về của câu truy vấn 22:20 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51725) |
| 11 | Bài 11. Các phép toán trong SQL 15:43 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51727) |
| 12 | Bài 12. Lọc dữ liệu bằng mệnh đề WHERE trong SQL 20:30 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51729) |
| 13 | Bài 13. Kết hợp điều kiện bằng toán tử AND, OR, NOT trong SQL 18:07 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51731) |
| 14 | Bài 14. Toán tử BETWEEN trong SQL 17:20 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51733) |
| 15 | Bài 15. Toán tử LIKE - lọc dữ liệu chuỗi trong SQL 12:54 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51735) |
| 16 | Bài 16. WILDCARD - Ký tự đại diện trong SQL 16:54 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51737) |
| 17 | Bài 17. Lọc dữ liệu trong danh sách bằng toán tử IN trong SQL 14:25 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51740) |
| 18 | Bài 18. Kiểm tra dữ liệu NULL trong SQL 09:59 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51742) |
| 19 | Bài 19. GROUP BY - Nhóm dữ liệu trong SQL 15:20 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51744) |
| 20 | Bài 20. DAY MONTH YEAR - các hàm lấy ngày tháng năm cơ bản trong SQL 15:21 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51746) |
| 21 | Bài 21. HAVING - Lọc dữ liệu sau GROUP BY 21:57 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51780) |
| 22 | Bài 22. Bài tập ôn tập câu lệnh SQL 27:38 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51783) |
| 23 | Bài 23. Truy vấn dữ liệu từ nhiều table 36:23 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51785) |
| 24 | Bài 24. Bài tập truy vấn dữ liệu từ nhiều Table khác nhau 19:24 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51844) |
| 25 | Bài 25. Câu lệnh Union - Kết hợp các kết quả 35:45 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51846) |
| 26 | Bài 26. Các câu lênh JOIN - LEFT JOIN - RIGHT JOIN - FULL JOIN 32:22 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51848) |
| 27 | Bài 27. Bài tập về các câu lệnh JOIN 18:42 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51851) |
| 28 | Bài 28. Sub Query | Nested Query - Truy vấn con, truy vấn lồng nhau 26:27 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51854) |
| 29 | Bài 29. Bài tập Sub Query - truy vấn con, truy vấn lồng nhau 14:33 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51856) |
| 30 | Bài 30. Thứ tự thực thi trong câu truy vấn SQL 16:52 | [Watch Lesson](https://titv.vn/courses-page/sql-server/51858) |
| 31 | Bài 31. Nâng cao hiệu suất truy vấn SQL với Common Table Expression (CTE) 48:16 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55377) |
| 32 | Bài 32. Cách xây dựng câu truy vấn đệ quy 37:04 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55378) |
| 33 | Bài 33. Windows Functions và các ứng dụng 30:25 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55380) |
| 34 | Bài 34. Phân biệt các nhóm lệnh trong SQL 25:35 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55381) |
| 35 | Bài 35. Cách tạo mới cơ sở dữ liệu 11:38 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55382) |
| 36 | Bài 36. Cách tạo, thay đổi cấu trúc và xóa Table 38:56 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55383) |
| 37 | Bài 37. Lưu ý về kiểu dữ liệu 20:49 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55386) |
| 38 | Bài 38. Câu lệnh INSERT INTO thêm dữ liệu vào bảng 18:56 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55387) |
| 39 | Bài 39. Câu lệnh SELECT INTO copy dữ liệu và tạo bảng mới 19:33 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55388) |
| 40 | Bài 40. Câu lệnh DELETE xóa dữ liệu trong bảng 12:26 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55389) |
| 41 | Bài 41. Câu lệnh UPDATE cập nhật dữ liệu 12:14 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55390) |
| 42 | Bài 42. Index trong cơ sở dữ liệu 49:53 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55391) |
| 43 | Bài 43. View trong cơ sở dữ liệu 22:21 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55392) |
| 44 | Bài 44. Giới thiệu về T SQL 11:54 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55393) |
| 45 | Bài 45. Stored Procedures trong SQL Server 42:43 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55394) |
| 46 | Bài 46. Triggers trong SQL Server 49:55 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55395) |
| 47 | Bài 47. Triển khai cơ sở dữ liệu trên nền tảng Microsoft Azure 59:39 | [Watch Lesson](https://titv.vn/courses-page/sql-server/55396) |
| 48 | [Video] Thị giác máy tính - Computer ... | [Watch Lesson](https://titv.vn/courses-page/video-thi-giac-may-tinh-computer-vision) |
| 49 | Cấu trúc dữ liệu và giải thuật Java | [Watch Lesson](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java) |
| 50 | [Video] Nguyên lý Hệ điều hành | [Watch Lesson](https://titv.vn/courses-page/he-dieu-hanh) |
| 51 | [Video] Quản lý project Java với Maven | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven) |
| 52 | Lập trình .NET Windows Form | [Watch Lesson](https://titv.vn/courses-page/windows-form) |
| 53 | [Video] Lập trình mạng (sử dụng Java) | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java) |

