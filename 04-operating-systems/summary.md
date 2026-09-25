# Domain: Operating Systems & Linux — Summary

## Current Level Assessment
- **OS Concepts & Principles**: 3/5 (Theory: 3/5, Practical: 2/5, Troubleshooting: 1/5, Design: 1/5) — *Verified via course theory lectures.*
- **Linux Administration & Bash**: 3/5 (Theory: 3/5, Practical: 3/5, Troubleshooting: 2/5, Design: 2/5) — *Verified via Ubuntu VM/WSL & Bash scripts.*
- **Linux System Programming**: 0/5 (Theory: 1/5, Practical: 0/5, Troubleshooting: 0/5, Design: 0/5) — *Unverified / Tracked for Future.*

> ⚠️ **Critical Distinction**: Understanding OS theory (CPU scheduling, Paging, PCB) does **NOT** equal mastering Linux Administration (FHS, Systemd, chmod, APT), and Linux Administration does **NOT** equal Linux System Programming (`fork`, `exec`, `epoll`, `pthread`).

---

## What I Have Learned

### 1. Operating System Concepts (Theory Verified)
- Hardware organization: CPU, Memory (RAM), I/O devices, Buses.
- Dual-mode CPU operation (User mode vs Kernel mode) & System Calls interface.
- Process concept: Process Control Block (PCB), Process States (New, Ready, Running, Waiting, Terminated).
- CPU Scheduling: Context switching, FCFS/FIFO, Round Robin, Priority Scheduling, Shortest Job First (SJF).
- Process Synchronization: Race conditions, Critical Section problem, Mutex, Semaphores.
- Deadlock: 4 necessary conditions (Mutual Exclusion, Hold & Wait, No Preemption, Circular Wait) & Prevention.
- Memory Management: Fixed/Variable Partitioning, Paging, Segmentation.
- File System abstractions and directory organization.

### 2. Linux Administration & Bash Scripting (Practical Verified)
- Ubuntu Linux installation on VirtualBox VM and Windows Subsystem for Linux (WSL).
- Linux Filesystem Hierarchy Standard (FHS): `/etc`, `/var`, `/usr`, `/bin`, `/boot`, `/home`, `/proc`, `/sys`.
- CLI Navigation & File operations: `pwd`, `cd`, `ls`, `mkdir`, `cp`, `mv`, `rm`, `cat`, `less`, `head`, `tail`.
- Text Searching & Regex: `grep`, `find`, `whereis`, `which`, Regular Expressions, Pipelines (`|`), Redirection (`>`, `>>`).
- Archiving & Editors: `tar`, `gzip`, `zip`, Vim editor modes (`:wq`).
- System Administration: Linux Boot process & Runlevels / Systemd targets, System monitoring (`top`, `df`, `du`, `free`, `uname`).
- User & Group Management: `sudo`, `useradd`, `groupadd`, `/etc/passwd`, `/etc/shadow`, `/etc/group`.
- Permissions & Links: `chmod` (symbolic/numeric), `chown`, `chgrp`, Hard links vs Soft/Symbolic links (`ln`).
- Software & Dev Tools: Package management (`apt`, `dpkg`), dev tools setup (GCC, Make, VS Code, JDK, Python, R).
- Bash Shell Scripting: `#!/bin/bash`, `read`, `echo`, arithmetic `$((...))`, positional parameters (`$1`), `if` conditions, `for`/`while` loops, arrays, functions, file I/O sorting, debugging (`bash -x`).

### 3. Linux System Programming (Future Tracked Knowledge Areas)
- POSIX System Calls: `fork()`, `exec()`, `wait()`, `waitpid()`.
- POSIX Threads & Synchronization: `pthread_create()`, `pthread_join()`, `pthread_mutex`, `sem_wait()`.
- Inter-Process Communication (IPC): Anonymous Pipes (`pipe()`), Named Pipes (FIFO), Shared Memory (`shm_open`), Unix Domain Sockets.
- High-Performance Event Demultiplexing: `select()`, `poll()`, `epoll()` kernel event loops.
- Kernel Diagnostics: `/proc` filesystem inspection, System call tracing with `strace`.

---

## Strong Areas
- Daily Linux CLI usage, terminal navigation, file manipulation, permission management (`chmod`), user admin.
- Writing Bash shell scripts for administration and task automation.
- Conceptual understanding of Process scheduling, PCB, IPC, and OS system calls.

## Weak Areas
- Linux System Programming: Never written POSIX C code using `fork()`, `pthread()`, `pipe()`, or `epoll()`.
- Advanced Linux Networking: Network Namespaces (`ip netns`), Linux Bridges, `iptables`/`nftables` NAT rules.
- Production Server Operations: Writing custom Systemd `.service` units, configuring Nginx reverse proxy, SSL certificates.

## Missing Knowledge (Tracked Gaps)
- **Linux System Programming**: `fork`, `exec`, `wait`, `pthread`, `mutex`, `semaphore`, `pipe`, `epoll`, `strace`, `/proc`.
- **Linux Container Primitives**: Linux Network Namespaces (`ip netns`), Cgroups, Namespaces (PID, Mount, Net), Linux Bridges.
- **Firewall & Routing**: `iptables`, `nftables`, IP Forwarding (`sysctl net.ipv4.ip_forward=1`), NAT rules.
- **Service Management**: Custom `systemd` `.service` unit files.

## Practical Gaps
- **OS Concepts**: Theory 3/5, Practical 2/5 (No POSIX C kernel/system programming labs).
- **Linux Admin**: Theory 3/5, Practical 3/5 (Ubuntu CLI & Bash scripts verified).
- **System Programming**: Theory 1/5, Practical 0/5 (No Evidence).

## Recommended Supplements
1. **Linux Network Namespaces & Bridges**: Practice `ip netns` and virtual bridge interface creation.
2. **Systemd Service Unit**: Write a `.service` file to run background Java web applications.
3. **POSIX C System Programming**: Perform basic `fork()`, `exec()`, and `pthread` system call labs.

## Readiness for Next Topics
- **Linux Daily Usage & Scripting**: **READY (3/5)**
- **Docker & Container Primitives**: **PARTIALLY READY (2/5)**
  - Linux CLI & Permissions: 3/5
  - Bash Scripting: 3/5
  - Linux Network Namespaces: 1/5
  - `iptables` / NAT: 1/5
  - *Action*: Bridge Linux networking gaps (`ip netns`, `iptables` NAT) before advanced Docker container networking.
