# Domain: Operating Systems & Linux — Summary

## Current Level
- **Overall**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## What I Have Learned
- Computer hardware organization, Dual-mode CPU operation, System Calls.
- Process states, Process Control Block (PCB), CPU Scheduling algorithms (FIFO, Round Robin, SJF).
- Inter-Process Communication (IPC), Race conditions, Semaphores, Mutex, Deadlock prevention.
- Memory management concepts (Paging, Segmentation, Fixed/Variable partitioning).
- File System abstractions and directory hierarchy.
- Linux Filesystem Hierarchy Standard (FHS), permissions (`chmod`), ownership (`chown`), links (`ln`).
- Linux CLI administration tools (`grep`, `find`, `tar`, `top`, `df`, `du`, `apt`, `useradd`, `systemd` runlevels).
- Vim text editor usage.
- Bash shell scripting: logic, loops, arrays, functions, file I/O, debugging.

## Strong Areas
- Daily Linux Terminal CLI usage, file manipulation, permission management, user management.
- Writing Bash shell scripts for administration and automation tasks.
- Conceptual understanding of Process scheduling, IPC, and OS system calls.

## Weak Areas
- Advanced Linux Networking (Network Namespaces, Linux Bridges, `iptables`/`nftables` NAT).
- Production Linux Server Deployment (Nginx, Systemd service unit creation, SSL/TLS setup).
- Low-level POSIX C system programming (`fork()`, `exec()`, `pipe()`).

## Missing Knowledge
- **Linux Container Primitives**: Linux Network Namespaces (`ip netns`), Cgroups, Namespaces (PID, Mount, Net), Linux Bridges.
- **Firewall & Routing**: `iptables`, `nftables`, IP Forwarding (`sysctl net.ipv4.ip_forward=1`), NAT rules.
- **Service Management**: Writing custom `systemd` `.service` units.

## Practical Gaps
- Theory Known: Linux OS Administration & Bash = 3/5.
- Practical Known: Linux CLI & Bash scripts in VM/WSL = 3/5.
- Practical Gap: Lacking hands-on Linux container networking configuration (`ip netns`, `veth` pairs, `iptables` NAT) required as Docker networking prerequisites.

## Depth Gaps
- OS Scheduling & Memory: Conceptual understanding high, but missing C system programming verification (`fork()`, `pthread`).

## Recommended Supplements
1. Practice Linux Network Namespaces & Virtual Ethernet pairs (`ip netns add ns1`, `ip link add veth0 type veth`).
2. Learn `iptables` NAT port forwarding rules.
3. Write systemd unit files to deploy Java web apps on Linux.

## Readiness
- **Docker & Containerization**: **PARTIALLY READY**
  - Linux CLI & Permissions: 3/5
  - Bash Scripting: 3/5
  - Linux Network Namespaces: 1/5
  - `iptables` / NAT: 1/5
  - *Reason*: Docker networking relies heavily on Linux Network Namespaces, bridge interfaces, and iptables NAT. Need to bridge Linux networking gaps before advanced Docker networking.
