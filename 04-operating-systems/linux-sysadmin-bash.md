# Linux System Administration & Bash Scripting (LPI 1-2)

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: High

## What I Have Learned
- **Linux Environment & Fundamentals**:
  - History of Linux, distributions (Ubuntu, Debian, RHEL).
  - Installing Ubuntu VM (VirtualBox/VMware) and configuring WSL (Windows Subsystem for Linux).
  - Linux Architecture (Kernel, Shell, System utilities).
  - Linux Filesystem Hierarchy Standard (FHS): `/`, `/bin`, `/boot`, `/dev`, `/etc`, `/home`, `/lib`, `/media`, `/opt`, `/proc`, `/root`, `/sbin`, `/sys`, `/tmp`, `/usr`, `/var`.
- **CLI Commands & System Management**:
  - Terminal navigation: `pwd`, `cd`, `ls` (`ls -la`), `clear`.
  - Directory & File operations: `mkdir`, `rmdir`, `touch`, `cp`, `mv`, `rm` (`rm -rf`), `cat`, `less`, `more`, `head`, `tail`.
  - Wildcards (`*`, `?`, `[]`).
  - Input/Output Redirection (`>`, `>>`, `<`) and Pipelines (`|`).
  - Text searching & regex: `grep`, `egrep`, Regular Expressions.
  - File search: `find`, `whereis`, `which`.
  - Compression & Archiving: `tar` (`tar -cvzf`, `tar -xvzf`), `gzip`, `zip`, `unzip`.
  - Text Editors: `vi` / `vim` editor (Normal, Insert, Command modes, navigation, save/exit `:wq`, `:q!`), `cut` command.
  - Date & Time: `date`, `cal`, system clock setup.
  - Power management: `shutdown`, `reboot`.
  - Linux Boot Process: BIOS/UEFI -> MBR/GPT -> GRUB -> Kernel -> Init/Systemd targets (Runlevels 0-6).
  - System Monitoring & Info: `uname`, `hostname`, `df -h`, `du -sh`, `top`, `free -m`, `uptime`.
  - User & Group Administration: `useradd`, `usermod`, `userdel`, `/etc/passwd`, `/etc/shadow`, `groupadd`, `groupmod`, `groupdel`, `/etc/group`, `sudo` privileges & `visudo`.
  - File Permissions & Ownership: `chmod` (symbolic `u+x`, numeric `755`, `644`), `chown`, `chgrp`.
  - Links: Hard Links vs Soft/Symbolic Links (`ln`, `ln -s`).
  - Linux File Systems & Storage: File system types (`ext4`, `xfs`), partition management (`fdisk`, `lsblk`, `mkfs`).
  - Package Management: `apt update`, `apt upgrade`, `apt install`, `apt remove`, `dpkg`.
  - Developer Tools Setup: Vietnamese IME, GCC/G++, Make, CodeBlocks, VS Code, Java JDK, Python/PyCharm, R/RStudio on Ubuntu.
- **Linux Networking Basics**:
  - Network commands: `ip addr`, `ifconfig`, `ping`, `netstat` / `ss`.
  - Static & Dynamic IP configuration: `/etc/netplan/` or `/etc/network/interfaces`.
- **Bash Shell Scripting**:
  - Script structure (`#!/bin/bash`), permissions (`chmod +x`).
  - Input/Output: `echo`, `read`.
  - Arithmetic operations: `expr`, `$((...))`, `bc`.
  - Script arguments: `$0`, `$1`, `$2`, `$#`, `$@`, `$*`.
  - Conditions & Comparisons: `if [ ... ]`, `elif`, `else`, `fi`, integer comparisons (`-eq`, `-ne`, `-gt`, `-ge`, `-lt`, `-le`), string comparisons (`==`, `!=`, `-z`).
  - Loops: `for`, `while`, `until` loops.
  - Shell Arrays: array declaration, indexing, length `${#arr[@]}`.
  - Shell Functions: function definition, parameter passing, return values.
  - Practical Shell Scripts: Prime number checking script, min element array finder, file I/O sorting script.
  - Bash Debugging: `bash -x script.sh`.

## What I Understand
- The Linux Filesystem Hierarchy Standard (FHS) and why system files are organized into `/etc` (config), `/var` (variable data/logs), `/bin` (executables), `/usr` (user applications).
- Symbolic link vs Hard link mechanisms (Hard links point to the same inode number; Symbolic links point to file path string).
- Linux file permission bitwise mechanism (User, Group, Others with Read=4, Write=2, Execute=1).
- Process execution pipeline and stream redirection (`stdin`=0, `stdout`=1, `stderr`=2).
- Linux boot sequence and Systemd target initialization.
- Bash shell script execution flow and variable scoping.

## What I Can Do
- Install and operate Ubuntu Linux via Desktop GUI, VirtualBox, WSL, and SSH Terminal CLI.
- Perform daily Linux system administration tasks: managing files, users, groups, permissions, disk space, and installed software packages.
- Write, test, and debug multi-featured Bash shell scripts for task automation.
- Search text files and logs using `grep`, `find`, and Regular Expressions.
- Configure Linux static IP addresses and inspect network ports.

## What I Cannot Yet Do
- Configure advanced Linux firewall rules using `iptables` / `nftables` or `ufw`.
- Manage Linux Network Namespaces, bridges, veth pairs, or TUN/TAP devices (prerequisites for Docker networking).
- Manage SELinux or AppArmor security profiles.
- Configure enterprise services: Nginx/Apache reverse proxies, BIND DNS servers, DHCP servers, NFS/Samba file sharing.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-008** — Hệ điều hành Linux LPI-1/2 (TITV) | URL: https://titv.vn/courses-page/video-he-djieu-hanh-linux-lpi-1-2/ | Lessons 01-55 (FHS, CLI, Permissions, Vim, Bash Scripting)
- **SRC-005** — Nguyên lý hệ điều hành (TITV) | URL: https://titv.vn/courses-page/he-dieu-hanh/ | OS Kernel & System call architecture

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Limited experience with advanced Linux networking (iptables, NAT, bridge networks, Network Namespaces).
- No production Linux server deployment experience (e.g., configuring Nginx, SSL certificates, systemd service units for Spring Boot apps).

## Missing Knowledge
- **Advanced Linux Networking**: `iptables`, `nftables`, Linux Bridge (`brctl`/`ip link`), NAT / IP Forwarding, Network Namespaces (`ip netns`).
- **Service Management**: Writing custom `systemd` `.service` unit files.
- **Web Server Admin**: Nginx reverse proxy & SSL (Certbot) configuration.

## Recommended Supplement
1. Practice Linux Network Namespaces, bridge creation, and NAT routing commands (`ip netns`, `ip link add type bridge`, `iptables -t nat`).
2. Write custom `systemd` service units to run background Java applications automatically.
3. Configure Nginx reverse proxy on Ubuntu Linux.
