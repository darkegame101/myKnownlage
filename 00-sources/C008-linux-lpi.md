# Course Summary: C008 — Hệ điều hành Linux (LPI 1-2)

## Course Overview
- **Course ID**: C008
- **Provider**: TITV
- **Course Name**: Hệ điều hành Linux (LPI 1-2)
- **URL**: [https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/)
- **Status**: Completed
- **Total Lectures**: 55 Video Lessons

## Topics Covered
1. **Linux Environment & Setup**: Linux overview, Ubuntu VM (VirtualBox) and WSL setup, Linux Architecture (Kernel, Shell, System calls), Filesystem Hierarchy Standard (FHS).
2. **CLI Commands & Utilities**: Terminal usage, `pwd`, `cd`, `ls`, `mkdir`, `cp`, `mv`, `rm`, `cat`, `less`, `more`, `head`, `tail`, wildcards, `grep`, `find`, `whereis`, `which`, `tar`, `gzip`, `zip`, `cut`, `date`, `cal`, `shutdown`, `reboot`.
3. **Vim & Text Manipulation**: Vim editor modes, navigation, editing, saving (`:wq`), Regular Expressions (Regex), Pipelines (`|`), I/O Redirection (`>`, `>>`).
4. **SysAdmin & User Management**: Linux Boot process & Runlevels / Systemd targets, System info (`uname`, `df`, `du`, `top`, `free`), `sudo`, User management (`useradd`, `/etc/passwd`), Group management (`groupadd`, `/etc/group`), File permissions (`chmod`), Ownership (`chown`), Hard vs Soft Links (`ln`).
5. **Software & Networking**: Package management (`apt`, `dpkg`), Dev tools setup (GCC, Make, VS Code, JDK, Python, R), Linux network config (`ip addr`, `ifconfig`, `ping`, `netstat`/`ss`), IP address setup.
6. **Bash Shell Scripting**: Shell intro (`#!/bin/bash`), input/output (`echo`, `read`), arithmetic calculations, parameters (`$1`, `$2`), conditions (`if`), loops (`for`, `while`), arrays, functions, math scripts (prime check, min array), file I/O & array sorting, Bash debugging (`bash -x`).

## Topics Already Known Before Course
- Basic OS concepts (from C005).

## New Knowledge Added
- Linux Filesystem Hierarchy Standard (FHS).
- Linux Terminal CLI administration commands.
- File permission bits (`chmod`), ownership (`chown`), hard vs soft links.
- Package management with `apt` and `dpkg`.
- Vim text editor usage.
- Bash Shell Scripting (logic, loops, arrays, functions, debugging).

## Knowledge Deepened
- Operating system file management and process concepts.

## Practical Skills Added
- Operating Ubuntu Linux via VirtualBox VM and WSL.
- System administration: managing files, permissions, users, and disk space.
- Writing and debugging Bash shell automation scripts.

## Remaining Gaps
- Linux Network Namespaces (`ip netns`), virtual bridges, `iptables` / `nftables` NAT rules.
- Writing custom `systemd` `.service` unit files.
- Nginx reverse proxy and SSL certificate setup.

## Knowledge Not Covered
- Linux Container primitives (Cgroups, Namespaces detail).
- Enterprise Linux server deployment (Nginx, Systemd services).

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
1. Practice Linux Network Namespaces & Virtual Ethernet pairs (`ip netns`).
2. Learn `iptables` NAT port forwarding rules.
3. Write `systemd` service unit files for Java apps.

## Lecture Index & Direct Lesson Links

Main Course Page: [https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/)

| # | Lecture / Lesson Title | Direct Lesson URL |
| :---: | :--- | :--- |
| 1 | Bài 01 - Giới thiệu khóa học Hệ điều hành Linux 28:07 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55471) |
| 2 | Bài 02 - Giới thiệu tổng quan về Hệ điều hành Linux 23:08 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55472) |
| 3 | Bài 03 - Cách cài đặt Ubuntu trên máy ảo 12:58 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55473) |
| 4 | Bài 04 - Hướng dẫn dùng WSL chạy Ubuntu Linux trên Windows 18:28 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55474) |
| 5 | Bài 05 - Cấu trúc của hệ điều hành Linux 11:52 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55475) |
| 6 | Bài 06 - Cấu trúc cây thư mục của hệ điều hành Linux 09:40 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55476) |
| 7 | Bài 07 - Cách sử dụng Terminal và cú pháp câu lệnh trong Linux 14:43 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55477) |
| 8 | Bài 08 - Lệnh Sudo và cách đặt mật khẩu cho tài khoản root trong Linux 09:49 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55478) |
| 9 | Bài 09 - Lệnh in thư mục hiện hành (pwd) và lệnh thay đổi thư mục (cd) của Linux 09:04 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55479) |
| 10 | Bài 10 - Các lệnh quản lý file và thư mục trong Linux 48:41 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55480) |
| 11 | Bài 11 - Các ký tự đại diện trong Linux 13:17 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55481) |
| 12 | Bài 12 - Các lệnh xem nội dung tập tin trong Linux 12:27 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55482) |
| 13 | Bài 13 - Định hướng nhập xuất và đường ống pipeline trong Linux 14:50 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55483) |
| 14 | Bài 14 - Câu lệnh tìm kiếm grep trong Linux 15:36 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55484) |
| 15 | Bài 15 - Biểu thức chính quy - Regular Expression Regex 21:09 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55485) |
| 16 | Bài 16 - Tìm kiếm tập tin bằng lệnh find trong Linux 29:37 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55486) |
| 17 | Bài 17 - Câu lệnh tìm kiếm whereis và which trong Linux 05:29 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55487) |
| 18 | Bài 18 - Câu lệnh nén và giải nén trong Linux 16:29 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55488) |
| 19 | Bài 19 - Hướng dẫn sử dụng trình soạn thảo vi 39:28 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55489) |
| 20 | Bài 20 - Thực hành trình soạn thảo vi 09:18 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55490) |
| 21 | Bài 21 - Lệnh CUT trong Linux 12:55 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55491) |
| 22 | Bài 22 - Các lệnh về ngày giờ trong Linux 13:49 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55492) |
| 23 | Bài 23 - Các lệnh tắt và khởi động lại máy trong Linux 06:27 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55493) |
| 24 | Bài 24 - Quá trình khởi động hệ điều hành Linux và các run levels 13:57 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55494) |
| 25 | Bài 25 - Các câu lệnh xem thông tin hệ thống Linux 19:05 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55712) |
| 26 | Bài 26 - Quản trị người dùng trong hệ thống Linux 13:28 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55713) |
| 27 | Bài 27 - Các câu lệnh quản trị người dùng trong hệ thống Linux 19:10 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55714) |
| 28 | Bài 28 - Quản trị group trong Linux 05:04 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55715) |
| 29 | Bài 29 - Các lệnh quản trị group trong Linux 08:55 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55716) |
| 30 | Bài 30 - Phân quyền trên hệ thống file và thư mục trong Linux 22:44 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55717) |
| 31 | Bài 31 - Các lệnh thay đổi quyền, người, nhóm sở hữu file và thư mục trong Linux 17:46 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55718) |
| 32 | Bài 32 - Hard Link và Soft Link Symbolic Link trong Linux 25:27 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55719) |
| 33 | Bài 33 - Cấu hình mạng trong Linux 17:21 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55720) |
| 34 | Bài 34 - Cấu hình địa chỉ IP trong Linux 13:13 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55721) |
| 35 | Bài 35 - Hướng dẫn cài đặt và gỡ bỏ ứng dụng trong Ubuntu 18:21 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55722) |
| 36 | Bài 36 - Hướng dẫn cài bộ gõ tiếng Việt trên Ubuntu 06:36 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55723) |
| 37 | Bài 37 - Hướng dẫn cài đặt công cụ lập trình C/C++ trong linux 08:04 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55724) |
| 38 | Bài 38 - Hướng dẫn cài đặt codeblocks để lập trình C/C++ trong Linux 04:07 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55725) |
| 39 | Bài 39 - Hướng dẫn cài đặt Visual Studio Code trong Ubuntu Linux 06:41 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55726) |
| 40 | Bài 40 - Hướng dẫn cài đặt công cụ lập trình Java trên Linux 14:26 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55765) |
| 41 | Bài 41 - Hướng dẫn cài đặt Python và công cụ lập trình Pycharm trên linux 13:09 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55766) |
| 42 | Bài 42 - Hướng dẫn cài đặt R và RStudio trong Linux 07:14 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55767) |
| 43 | Bài 43 - Linux File Systems và một số câu lệnh quản lý phân vùng 07:50 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55768) |
| 44 | Bài 44 - Giới thiệu về lập trình Shell Bash trong Linux 10:10 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55769) |
| 45 | Bài 45 - Câu lệnh nhập và xuất trong lập trình Shell 14:52 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55771) |
| 46 | Bài 46 - Thực hiện các phép tính trong lập trình Shell Bash 25:58 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55773) |
| 47 | Bài 47 - Truyền tham số lệnh Shell Bash 09:44 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55774) |
| 48 | Bài 48 - Câu lệnh điều kiện và các phép toán so sánh trong Shell Bash 30:14 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55775) |
| 49 | Bài 49 - Vòng lặp trong Shell Bash 19:14 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55776) |
| 50 | Bài 50 - Cách sử dụng mảng trong lập trình Shell Bash 16:12 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55784) |
| 51 | Bài 51 - Cách xây dựng hàm trong lập trình Shell Bash 10:58 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55785) |
| 52 | Bài 52 - Lập trình kiểm tra số nguyên tố 10:37 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55786) |
| 53 | Bài 53 - Lập trình tìm min của mảng trong Shell Bash 07:48 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55787) |
| 54 | Bài 54 - Nhập xuất dữ liệu từ file và sắp xếp mảng trong Shell Bash 14:43 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55788) |
| 55 | Bài 55 - Cách Debug trong lập trình Shell Bash 08:10 | [Watch Lesson](https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/55789) |
| 56 | [Video] Thị giác máy tính - Computer ... | [Watch Lesson](https://titv.vn/courses-page/video-thi-giac-may-tinh-computer-vision) |
| 57 | Cấu trúc dữ liệu và giải thuật Java | [Watch Lesson](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java) |
| 58 | [Video] Nguyên lý Hệ điều hành | [Watch Lesson](https://titv.vn/courses-page/he-dieu-hanh) |
| 59 | [Video] SQL Server - Cơ bản và Nâng cao | [Watch Lesson](https://titv.vn/courses-page/sql-server) |
| 60 | [Video] Lập trình Java (Java Core) | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-java-java-core) |
| 61 | [Video] Lập trình C | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-c) |

