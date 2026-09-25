# Course Summary: C006 — Lập trình mạng (sử dụng Java)

## Course Overview
- **Course ID**: C006
- **Provider**: TITV
- **Course Name**: Lập trình mạng (sử dụng Java)
- **URL**: [https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/)
- **Status**: Completed
- **Total Lectures**: 34 Video Lessons

## Topics Covered
1. **Networking Intro & Java I/O**: Network applications overview, NetBeans setup, NSLOOKUP app (`InetAddress`), Stream I/O review, File operations, Logging best practices, Card manager app.
2. **Multithreading**: Multi-threading concept (`Thread`, `Runnable`), Producer-Consumer problem, Thread Synchronization (`synchronized`), Multi-threaded Library Manager app.
3. **URL & TCP Socket Programming**: `InetAddress`, `URL`, `URLConnection`, TCP Socket intro (`Socket`, `ServerSocket`), 1-on-1 Chat app, Multi-client Chat Room Server, Remote Desktop Control GUI application project.
4. **UDP Datagram Programming**: UDP Protocol intro, `DatagramSocket`, `DatagramPacket`, UDP Send/Receive app, UDP DNS Domain Name Resolution simulator project.
5. **Multicast & RMI**: Multicast intro (`MulticastSocket`), Multicast Sender/Receiver, Lightstick control simulation via Multicast, Remote Method Invocation (RMI) intro.

## Topics Already Known Before Course
- Java Core Syntax (from C001).
- Basic File I/O (from C001).

## New Knowledge Added
- Java IP Address handling (`InetAddress`).
- Java TCP Socket programming (`Socket`, `ServerSocket`).
- Java UDP Datagram programming (`DatagramSocket`, `DatagramPacket`).
- Multicast packet broadcasting (`MulticastSocket`).
- Multi-threading synchronization in network socket servers (`synchronized`).
- Distributed objects with Java RMI.

## Knowledge Deepened
- Multithreaded application execution and shared state synchronization.
- Character and Byte stream I/O over network sockets.

## Practical Skills Added
- Building multi-client TCP Chat Room server apps.
- Building Remote Desktop GUI application in Java.
- Building UDP DNS Simulator app and Multicast controller app.

## Remaining Gaps
- Wireshark / `tcpdump` live packet capture and inspection.
- Java Non-blocking I/O (NIO / `java.nio`).
- SSL/TLS Socket encryption (`SSLSocket`, HTTPS).
- CIDR Subnetting, NAT, and router/switch infrastructure configuration.

## Knowledge Not Covered
- HTTP/1.1, HTTP/2, WebSockets protocol depth.
- Wireshark packet capture analysis.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
1. Practice Wireshark packet capture on TCP handshakes and HTTP requests.
2. Study CIDR subnetting and NAT IP translation.

## Lecture Index & Direct Lesson Links

Main Course Page: [https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/)

| # | Lecture / Lesson Title | Direct Lesson URL |
| :---: | :--- | :--- |
| 1 | 1. Giới thiệu nội dung khóa học | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52438) |
| 2 | 2. Tổng quan về mạng Internet và ứng dụng mạng | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52439) |
| 3 | 3. Tổng quan về mạng Internet và ứng dụng mạng (phần 2) | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52440) |
| 4 | 4. Cài đặt công cụ lập trình Netbeans | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52441) |
| 5 | 5. Thực hành - Xây dựng ứng dụng NSLOOKUP đơn giản | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52442) |
| 6 | 6. Giới thiệu về nhập xuất trong Java | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52477) |
| 7 | 7. Ví dụ về nhập xuất đơn giản | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52478) |
| 8 | 8. Luồng dữ liệu | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52479) |
| 9 | 9. Các lớp quan trọng trong Java dùng để nhập xuất dữ liệu | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52480) |
| 10 | 10. Thực hành - bài tập tạo File | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52481) |
| 11 | Thực hành - bài tập kiểm tra các quyền truy xuất File | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52482) |
| 12 | 11. Thực hành: cây thư mục | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52567) |
| 13 | 12. Thực hành: xóa file/thư mục | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52568) |
| 14 | 13. Thực hành: thay đổi tên file | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52569) |
| 15 | 14. Thực hành: copy file hoặc thư mục | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52570) |
| 16 | Bài tập tự làm: di chuyển file/ thư mục | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52571) |
| 17 | 15. Lưu ý về ghi Log trong lập trình | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52631) |
| 18 | 16. Thực hành - ghi và đọc dữ liệu từ file text | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52632) |
| 19 | 17. Thực hành đọc và ghi đối tượng, xây dựng phần mềm quản lý danh thiếp | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52832) |
| 20 | 18. Giới thiệu về lập trình đa tiến trình - Multi Threading | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52975) |
| 21 | 19. Thực hành lập trình đa tiến trình - bài toán nhà sản xuất và người tiêu dùng | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52976) |
| 22 | 20. Đồng bộ hóa tiến trình - synchronized | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52977) |
| 23 | 21. Thực hành xây dựng ứng dụng quản lý thư viện sử dụng đa tiến trình | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/52978) |
| 24 | 22. Địa chỉ mạng InetAddress | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53063) |
| 25 | 23. Kết nối và truy xuất dữ liệu từ URL | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53065) |
| 26 | 24. Giới thiệu về lập trình Socket | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53067) |
| 27 | 25. Xây dựng ứng dụng chat đơn giản Client - Server | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53070) |
| 28 | 26. Thực hành - xây dựng ứng dụng Chat Room | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53166) |
| 29 | 27. Thực hành - xây dựng ứng dụng điều khiển máy tính từ xa - Remote Desktop | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53179) |
| 30 | 28. Giới thiệu giao thức UDP | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53520) |
| 31 | 29. Thực hành gửi và nhận tin qua giao thức UDP | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53523) |
| 32 | 30. Thực hành - giả lập hệ thống phân giải tên miền DNS dựa trên giao thức UDP | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53526) |
| 33 | 31. Giới thiệu lập trình Multicast | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53527) |
| 34 | 32. Thực hành gửi tin Multicast | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53529) |
| 35 | 33. Thực hành đểu khiển lightstick bằng Multicast | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53531) |
| 36 | 34. Lập trình phân tán đối tượng với RMI | [Watch Lesson](https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/53534) |
| 37 | [Video] Thị giác máy tính - Computer ... | [Watch Lesson](https://titv.vn/courses-page/video-thi-giac-may-tinh-computer-vision) |
| 38 | Cấu trúc dữ liệu và giải thuật Java | [Watch Lesson](https://titv.vn/courses-page/video-cau-truc-du-lieu-va-giai-thuat-java) |
| 39 | [Video] Nguyên lý Hệ điều hành | [Watch Lesson](https://titv.vn/courses-page/he-dieu-hanh) |
| 40 | [Video] SQL Server - Cơ bản và Nâng cao | [Watch Lesson](https://titv.vn/courses-page/sql-server) |
| 41 | Lập trình .NET Windows Form | [Watch Lesson](https://titv.vn/courses-page/windows-form) |

