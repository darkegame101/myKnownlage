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
