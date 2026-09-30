# Assessment Instrument: P004 — Linux Process & Network Diagnostics

## 📌 Project Overview
- **Project ID**: `P004`
- **Project Name**: Linux Process & Network Diagnostics
- **Domain**: Operating Systems & Linux Systems Administration
- **Status**: Planned
- **Evidence Status**: No Evidence
- **Repository**: TBD
- **Assessment Date**: Pending
- **Target Score**: Practical 4/5, Troubleshooting 4/5, Theory 4/5

---

## 🎯 1. Goal & Rationale
- **Goal**: Execute deep OS-level diagnostics inside a Linux environment (Ubuntu/Debian or WSL2), inspecting process lifecycles, signals, open file descriptors via `/proc`, system call tracing via `strace`, configuring a custom `systemd` service daemon, and building isolated network namespaces with virtual ethernet pairs.
- **Why this project exists**: Previous work ([`C008`](../00-sources/C008-linux-bash.md) / [`P-HIST-004`](./project-log.md#entry-p-hist-004--linux-server-administration--bash-automation-suite)) proved basic shell commands and Bash scripts (Level 3/5). However, deploying microservices and understanding Docker containers requires deeper systems knowledge: process states, file descriptors, system calls, systemd supervision, and Linux network namespaces.

---

## 📋 2. Prerequisites
- Linux Terminal CLI & Permissions (Level 3/5)
- Bash Scripting & Automation (Level 3/5)
- OS Principles: Processes, Scheduling, Virtual Memory (Level 3/5)

---

## 🔬 3. Skills Being Assessed

### A. Theory Assessed
- Process lifecycle and states: Running (R), Interruptible Sleep (S), Uninterruptible Sleep (D), Stopped (T), and Zombie (Z).
- Inter-Process Communication & Signals: `SIGTERM` (15), `SIGKILL` (9), `SIGHUP` (1), `SIGINT` (2).
- The Linux `/proc` pseudo-filesystem: How the kernel exposes kernel structures and hardware states to user space.
- System calls: How user-space applications invoke kernel routines (`openat`, `read`, `write`, `socket`, `clone`).
- Linux Network Namespaces (`netns`): How the kernel provides network stack isolation for containers.

### B. Practical Skills Assessed
- Writing and deploying a custom `systemd` service unit file (`/etc/systemd/system/myapp.service`) with auto-restart, dedicated user, and log redirection.
- Inspecting active listening TCP/UDP sockets using `ss -tulpn`.
- Inspecting open file descriptors and socket handles for a specific PID using `lsof` and `/proc/<pid>/fd/`.
- Building and connecting two isolated network namespaces using `veth` (Virtual Ethernet) pairs.

### C. Troubleshooting Skills Assessed
- Diagnosing a high CPU or memory-leaking process using `top`, `ps aux --sort=-%mem`, and `vmstat`.
- Using `strace -p <pid> -e trace=file,network` to identify why an application fails to start or open configuration files.
- Investigating and terminating unkillable/zombie processes.

### D. Design Skills Assessed
- Designing a robust `systemd` unit file with security constraints (`ProtectSystem=strict`, `NoNewPrivileges=true`).
- Designing an isolated virtual network topology on a single Linux host using bridge interfaces.

---

## 🧪 4. Required Hands-on Experiments

All terminal sessions, command inputs, and outputs must be captured in markdown logs within the repository:

### Experiment 1: Process Lifecycle, Signals & Zombie Analysis
1. Write a simple Python or C script that spawns a child process and has the parent sleep without calling `wait()` / `waitpid()`.
2. Inspect the process table: Prove the child enters state `Z` (Zombie / Defunct).
3. Demonstrate why `kill -9 <child_pid>` cannot kill a zombie process (because it is already dead).
4. Terminate the parent process and show how `systemd` (PID 1) inherits and reaps the zombie child.
5. Demonstrate graceful shutdown by trapping `SIGTERM` in a Bash or Java process to flush logs before exit.

### Experiment 2: The `/proc` Filesystem Deep Dive
Select an active service (e.g. Nginx, SSHD, or a Java app) with known PID:
1. Cat `/proc/<pid>/status`: Document `VmRSS` (Resident Set Size), `VmData`, and `Threads`.
2. Inspect `/proc/<pid>/cmdline` and `/proc/<pid>/environ`.
3. List open file descriptors in `/proc/<pid>/fd/`: Identify standard input (0), standard output (1), standard error (2), configuration files, and open network socket inodes.
4. Cross-reference the socket inode with `/proc/net/tcp` to find the exact local and remote IP:Port.

### Experiment 3: System Call Tracing with `strace`
1. Run a command or service that fails due to missing permissions or missing files.
2. Trace it using `strace -f -e trace=open,openat,access,connect <command> 2>&1 | tee trace.log`.
3. Highlight the exact `ENOENT` (No such file) or `EACCES` (Permission denied) system call that caused the application crash.
4. Trace a network client: Identify the `socket()`, `connect()`, `sendto()`, and `recvfrom()` syscalls.

### Experiment 4: Production `systemd` Daemon Configuration
1. Write a custom background worker script or Java JAR application.
2. Create `/etc/systemd/system/app-worker.service`:
   - Set `User=appuser`, `WorkingDirectory=/opt/app`.
   - Set `Restart=always`, `RestartSec=5s`.
   - Set `StandardOutput=journal`, `StandardError=journal`.
3. Test daemon controls: `systemctl daemon-reload`, `start`, `status`, `stop`, `enable`.
4. Intentionally kill the process with `kill -9 <pid>`: Prove that `systemd` automatically detects the unexpected exit and restarts the process within 5 seconds.
5. Query logs using `journalctl -u app-worker.service -n 50 --no-pager`.

### Experiment 5: Linux Network Namespaces & Virtual Ethernet (Container Prerequisite)
Build manual network isolation without Docker:
1. Create two isolated network namespaces:
   ```bash
   ip netns add red
   ip netns add blue
   ```
2. Create a virtual ethernet pair:
   ```bash
   ip link add veth-red type veth peer name veth-blue
   ```
3. Assign each end to its respective namespace:
   ```bash
   ip link set veth-red netns red
   ip link set veth-blue netns blue
   ```
4. Assign IP addresses and bring interfaces up:
   - Inside `red`: `10.0.0.1/24`
   - Inside `blue`: `10.0.0.2/24`
5. Execute `ip netns exec red ping 10.0.0.2`: Prove bi-directional ICMP reachability between isolated namespaces.
6. Clean up resources cleanly.

---

## 🛑 5. Acceptance Criteria

| Area | Minimum Required Evidence | Advanced Proof |
| :--- | :--- | :--- |
| **Process Inspection** | Clear demonstration of PID, PPID, signals, and zombie lifecycle analysis. | Memory leak tracking via RSS monitoring over time. |
| **`/proc` Filesystem** | Mapping file descriptor numbers to underlying disk files and socket inodes. | Inspecting `/proc/sys/net/ipv4/` kernel parameters. |
| **`strace` Diagnostics** | Filtered `strace` output pinpointing an exact root-cause failure syscall. | Tracing multi-threaded applications with `-f` showing thread creation (`clone`). |
| **`systemd` Supervision** | Functional unit file with verified automatic restart on abnormal termination. | Configuring `systemd-notify` Type=notify watchdog. |
| **Network Namespaces** | Successfully pinging across two distinct network namespaces via `veth` pair. | Connecting namespaces to a Linux bridge (`br0`) with `iptables` NAT for internet access. |

---

## 🚫 6. What This Project Does NOT Prove
- Does **NOT** prove writing Linux Kernel Modules in C.
- Does **NOT** prove high-level Docker Compose orchestrations (this lab evaluates the underlying Linux primitives).

---

## 📥 7. Project Submission Form

*Copy this block and fill it out when submitting your completed diagnostics lab to AI for assessment:*

```markdown
Project ID: P004
Project Name: Linux Process & Network Diagnostics
Repository URL: [Your GitHub Repo URL]
Commit SHA / Branch / PR: [Commit Hash]
Date: [YYYY-MM-DD]

### 1. Environment Details
- Linux Distribution & Kernel version: [e.g., Ubuntu 22.04 LTS / 5.15.0]
- Platform: [WSL2 / VirtualBox / Bare metal / Cloud VPS]

### 2. Experiments Evidence
- Zombie process reproduction log: [File link]
- `/proc/<pid>/fd` mapping output: [File link]
- `strace` failure diagnosis log: [File link]
- `systemd` service unit file & restart test: [File link]
- Network namespaces ping test: [File link]

### 3. Key Diagnostic Discoveries
- What root cause did `strace` uncover that error messages hid?
- How did the `veth` pair route packets without physical hardware?
```
