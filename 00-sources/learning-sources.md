# Master Learning Sources Registry (`learning-sources.md`)

Master catalog tracking all learning sources, courses, tutorials, and documentation (past, current, and planned). This file serves as the canonical single source of truth for all learning inputs and maps directly to the Knowledge Base.

---

## 📊 Learning Sources Summary Table

| ID | Domain | Topic | Source / Course | Provider | Type | Status | Verification | Coverage Confidence | Last Verified |
| :---: | :--- | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **SRC-001** | Programming | Java Core | [Lập trình Java – Java Core](https://titv.vn/courses-page/lap-trinh-java-java-core/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-002** | Programming | Data Structures & Algorithms | [Cấu trúc dữ liệu và giải thuật Java](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-003** | Database | SQL | [SQL Server](https://titv.vn/courses-page/sql-server/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-004** | Database | JDBC / Database Programming | [Lập trình Java tương tác CSDL](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-005** | Computer Systems | Operating Systems | [Nguyên lý hệ điều hành](https://titv.vn/courses-page/he-dieu-hanh/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-006** | Networking | Network Programming | [Lập trình mạng sử dụng Java](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-007** | Tools | Git / GitHub | [Git và GitHub toàn tập](https://titv.vn/courses-page/git-va-github-toan-tap/) | TITV | Course | Completed | Verified | High | 2026-09-26 |
| **SRC-008** | Computer Systems | Linux | [Hệ điều hành Linux LPI-1/2](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/) | TITV | Course | Completed | Verified | High | 2026-09-26 |

---

## 📌 Detailed Source Records & Source $\rightarrow$ Knowledge Mapping

### SRC-001
- **Domain**: Programming
- **Topic**: Java Core
- **Course**: Lập trình Java – Java Core
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/lap-trinh-java-java-core/](https://titv.vn/courses-page/lap-trinh-java-java-core/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (111 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Environment setup (JDK, Eclipse)
  - Primitive Data Types & Variables
  - Casting & Type Conversion
  - Operators & Math Class
  - Control Flow (`if-else`, `switch-case`)
  - Loops (`for`, `while`, `do-while`, `break`, `continue`)
  - 1D & 2D Arrays
  - String manipulation & `Comparable`
  - OOP Pillars: Encapsulation, Inheritance, Polymorphism, Abstraction
  - Interfaces & Abstract Classes
  - Packages & Access Modifiers (`public`, `protected`, `private`)
  - Exceptions handling (`try-catch-finally`)
  - Java Collections Framework (`ArrayList`, `Stack`, `Queue`, `Set`, `Map`, `Generics`)
  - File I/O Streams, Character/Byte Streams, Object Serialization, Zip/Unzip
  - Java Swing GUI, MVC Pattern, Layout Managers, Event Handling, Component Drag & Drop, Export JAR
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`01-programming/java-core.md`](../01-programming/java-core.md)
  - $\rightarrow$ [`01-programming/oop-java.md`](../01-programming/oop-java.md)
  - $\rightarrow$ [`00-sources/C001-java-core.md`](./C001-java-core.md)

---

### SRC-002
- **Domain**: Programming
- **Topic**: Data Structures & Algorithms
- **Course**: Cấu trúc dữ liệu và giải thuật Java
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java/](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (21 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Introduction to Data Structures & Algorithms
  - Big O Time & Space Complexity analysis
  - 1D Array operations & Exercises
  - 2D Array operations & Exercises
  - Generics in Java (`<T>`)
  - Singly Linked List Node Architecture & Pointer Traversal
  - Custom Singly Linked List Implementation in Java
  - Student Management exercise using Linked List
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`02-dsa/data-structures-algorithms-java.md`](../02-dsa/data-structures-algorithms-java.md)
  - $\rightarrow$ [`00-sources/C002-dsa-java.md`](./C002-dsa-java.md)

---

### SRC-003
- **Domain**: Database
- **Topic**: SQL
- **Course**: SQL Server
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/sql-server/](https://titv.vn/courses-page/sql-server/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (53 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - SQL Server 2022 & SSMS setup
  - DQL: `SELECT`, `SELECT DISTINCT`, `SELECT TOP`, Aliases (`AS`)
  - Aggregations: `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
  - Filtering & Sorting: `WHERE`, `ORDER BY`, `AND`, `OR`, `NOT`, `BETWEEN`, `LIKE`, `IN`, `IS NULL`
  - Grouping: `GROUP BY`, `HAVING`, Date functions (`DAY`, `MONTH`, `YEAR`)
  - Multi-table Queries: `UNION`, `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`
  - Advanced DQL: Subqueries (Nested queries), Query Execution Order, CTE (Common Table Expression), Recursive CTE, Window Functions (`ROW_NUMBER`, `RANK`, `DENSE_RANK`)
  - DDL: `CREATE DATABASE`, `CREATE/ALTER/DROP TABLE`
  - DML: `INSERT INTO`, `SELECT INTO`, `DELETE`, `UPDATE`
  - Database Objects: Clustered vs Non-clustered Indexes, Views, T-SQL Stored Procedures, Triggers, Azure SQL deployment intro
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`03-databases/sql-server.md`](../03-databases/sql-server.md)
  - $\rightarrow$ [`00-sources/C003-sql-server.md`](./C003-sql-server.md)

---

### SRC-004
- **Domain**: Database
- **Topic**: JDBC / Database Programming
- **Course**: Lập trình Java tương tác CSDL
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/](https://titv.vn/courses-page/lap-trinh-java-tuong-tac-csdl/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (14 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - JDBC Architecture & Driver Manager
  - Establishing database connections (`DriverManager.getConnection`)
  - Statement & ResultSet execution
  - PreparedStatement with parameterized SQL (`?`)
  - SQL Injection vulnerability & prevention
  - Data Access Object (DAO) Pattern (`DAOInterface<T>`)
  - Implementing concrete DAO classes for Java Model entities
  - SQL Type to Java Type mapping
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`03-databases/java-jdbc.md`](../03-databases/java-jdbc.md)
  - $\rightarrow$ [`00-sources/C004-java-jdbc.md`](./C004-java-jdbc.md)

---

### SRC-005
- **Domain**: Computer Systems
- **Topic**: Operating Systems
- **Course**: Nguyên lý hệ điều hành
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/he-dieu-hanh/](https://titv.vn/courses-page/he-dieu-hanh/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (24 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Computer Organization & Hardware abstraction
  - Operating System Services & System Calls (API)
  - Dual-mode CPU operation (User mode vs Kernel mode)
  - Process concept, Process Control Block (PCB), Process States
  - CPU Scheduling algorithms (FIFO/FCFS, Round Robin, Priority, SJF)
  - Inter-Process Communication (IPC) & Synchronization
  - Race conditions, Critical Section problem, Mutex, Semaphores
  - Deadlock 4 necessary conditions & prevention strategies
  - Memory Management, Partitioning, Paging, Segmentation
  - File System concepts & directory structures
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`04-operating-systems/os-concepts.md`](../04-operating-systems/os-concepts.md)
  - $\rightarrow$ [`00-sources/C005-os-concepts.md`](./C005-os-concepts.md)

---

### SRC-006
- **Domain**: Networking
- **Topic**: Network Programming
- **Course**: Lập trình mạng sử dụng Java
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (41 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Network applications & InetAddress IP handling
  - Java Stream I/O review & Logging best practices
  - Java Multithreading (`Thread`, `Runnable`), Producer-Consumer problem
  - Thread Synchronization (`synchronized` keyword)
  - `URL` and `URLConnection` data retrieval
  - TCP Socket Programming (`Socket`, `ServerSocket`)
  - 1-on-1 Chat application & Multi-client Chat Room Server
  - Remote Desktop Control GUI Application project
  - UDP Datagram Programming (`DatagramSocket`, `DatagramPacket`)
  - UDP DNS Name Resolution Simulator project
  - Multicast Programming (`MulticastSocket`), Lightstick Controller simulation
  - Java Remote Method Invocation (RMI) distributed objects
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`05-networking/java-network-programming.md`](../05-networking/java-network-programming.md)
  - $\rightarrow$ [`01-programming/java-core.md`](../01-programming/java-core.md) *(File I/O refresher overlap)*
  - $\rightarrow$ [`00-sources/C006-java-network.md`](./C006-java-network.md)

---

### SRC-007
- **Domain**: Tools
- **Topic**: Git / GitHub
- **Course**: Git và GitHub toàn tập
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/git-va-github-toan-tap/](https://titv.vn/courses-page/git-va-github-toan-tap/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (30 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Version Control System (VCS) fundamentals
  - Git CLI installation & user identity configuration (`user.name`, `user.email`)
  - 3 Git States (Working Directory, Staging Area, Repository)
  - Core commands: `git init`, `git add`, `git commit`, `git status`, `git diff`, `git log`
  - `.gitignore` configuration
  - Branching: `git branch`, `git checkout`, `git switch`, deleting branches
  - Merging: Fast-forward merge vs 3-way merge (`git merge`)
  - Rebasing: `git rebase` for linear history
  - Merge Conflict identification & manual resolution
  - History manipulation: Detached HEAD, `git reset` (soft, mixed, hard), `git revert`
  - GitHub Remote Collaboration: `git remote`, `git push`, `git pull`, `git clone`
  - Forking repositories & GitHub Pull Requests (PR) workflow
  - VS Code Git integration & GitHub Desktop GUI
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`06-devops-tools/git-github.md`](../06-devops-tools/git-github.md)
  - $\rightarrow$ [`00-sources/C007-git-github.md`](./C007-git-github.md)

---

### SRC-008
- **Domain**: Computer Systems
- **Topic**: Linux
- **Course**: Hệ điều hành Linux LPI-1/2
- **Provider**: TITV
- **URL**: [https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/)
- **Source Type**: Online Video Course
- **Status**: Completed
- **Verification Status**: Verified (61 lessons curriculum verified)
- **Last Verified**: 2026-09-26
- **Coverage Confidence**: High
- **Coverage**:
  - Linux Architecture & Filesystem Hierarchy Standard (FHS: `/etc`, `/var`, `/usr`, `/bin`)
  - Ubuntu VirtualBox VM & WSL setup on Windows
  - CLI Navigation & File management: `pwd`, `cd`, `ls`, `mkdir`, `cp`, `mv`, `rm`, `cat`, `less`, `head`, `tail`
  - Text search: `grep`, `find`, `whereis`, `which`, Regular Expressions (Regex)
  - Pipelines (`|`) & Stream Redirection (`>`, `>>`)
  - Archiving & Compression: `tar`, `gzip`, `zip`
  - Text Editors: Vim editor modes, navigation, editing, saving (`:wq`)
  - SysAdmin: Linux Boot process & Runlevels / Systemd targets
  - System Monitoring: `top`, `df`, `du`, `free`, `uname`, `uptime`
  - User & Group Management: `sudo`, `useradd`, `groupadd`, `/etc/passwd`, `/etc/shadow`
  - Permissions & Links: `chmod`, `chown`, `chgrp`, Hard links vs Soft/Symbolic links (`ln`)
  - Package Management: `apt`, `dpkg`
  - Dev Tools setup: GCC, Make, VS Code, JDK, Python, R on Ubuntu
  - Basic Networking config: `ip addr`, `ifconfig`, `ping`, `netstat`/`ss`, static IP setup
  - Bash Shell Scripting: `#!/bin/bash`, `read`, `echo`, arithmetic `$((...))`, parameters (`$1`), conditions (`if`), loops (`for`, `while`), arrays, functions, debugging (`bash -x`)
- **Source $\rightarrow$ Knowledge Mapping**:
  - $\rightarrow$ [`04-operating-systems/linux-sysadmin-bash.md`](../04-operating-systems/linux-sysadmin-bash.md)
  - $\rightarrow$ [`00-sources/C008-linux-lpi.md`](./C008-linux-lpi.md)

---

## 🔄 Knowledge $\rightarrow$ Source Summary Mapping Matrix

| Knowledge Base File | Mapped Source IDs | Primary Contributor | Overlap / Secondary Contributor |
| :--- | :---: | :--- | :--- |
| [`01-programming/java-core.md`](../01-programming/java-core.md) | **SRC-001**, **SRC-006** | **SRC-001** (Java Core) | **SRC-006** (File I/O refresher) |
| [`01-programming/oop-java.md`](../01-programming/oop-java.md) | **SRC-001** | **SRC-001** (Java Core) | — |
| [`02-dsa/data-structures-algorithms-java.md`](../02-dsa/data-structures-algorithms-java.md) | **SRC-002**, **SRC-001** | **SRC-002** (Java DSA) | **SRC-001** (Array & Collections) |
| [`03-databases/sql-server.md`](../03-databases/sql-server.md) | **SRC-003** | **SRC-003** (SQL Server) | — |
| [`03-databases/java-jdbc.md`](../03-databases/java-jdbc.md) | **SRC-004**, **SRC-003** | **SRC-004** (Java JDBC) | **SRC-003** (SQL Query review) |
| [`04-operating-systems/os-concepts.md`](../04-operating-systems/os-concepts.md) | **SRC-005** | **SRC-005** (OS Concepts) | — |
| [`04-operating-systems/linux-sysadmin-bash.md`](../04-operating-systems/linux-sysadmin-bash.md) | **SRC-008**, **SRC-005** | **SRC-008** (Linux LPI) | **SRC-005** (OS principles) |
| [`05-networking/java-network-programming.md`](../05-networking/java-network-programming.md) | **SRC-006** | **SRC-006** (Java Network) | — |
| [`06-devops-tools/git-github.md`](../06-devops-tools/git-github.md) | **SRC-007** | **SRC-007** (Git & GitHub) | — |
