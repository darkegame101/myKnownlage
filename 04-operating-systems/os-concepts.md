# Operating System Concepts

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 1/5
- **Confidence**: High

## What I Have Learned
- **Computer Hardware & OS Architecture**:
  - Computer organization: CPU, Memory (RAM), I/O devices, Buses.
  - OS definition, role as resource manager and hardware abstraction layer.
  - OS Services: User interface, program execution, I/O operations, file system manipulation, communications, error detection, resource allocation, protection and security.
  - System Calls & API: Dual-mode operation (User mode vs Kernel mode), system call interface (`read`, `write`, `fork`, `exec`).
  - OS Components: Kernel, Shell, System utilities.
  - Overview of modern OS architectures (Monolithic, Microkernel, Hybrid).
- **Process & Thread Management**:
  - Process concept: Process Control Block (PCB), process states (New, Ready, Running, Waiting, Terminated).
  - CPU Scheduling: Context switching, scheduling queues, Schedulers (FIFO/FCFS, Round Robin, Priority Scheduling, Shortest Job First - SJF).
  - Inter-Process Communication (IPC) and Concurrent Processes.
  - Process Synchronization: Race conditions, Critical Section problem, Mutex, Semaphores.
  - Deadlock: 4 necessary conditions for deadlock (Mutual Exclusion, Hold and Wait, No Preemption, Circular Wait), deadlock prevention and avoidance strategies.
- **Memory Management**:
  - Memory hierarchy (Registers, Cache, Main Memory, Secondary Storage).
  - Memory allocation schemes: Fixed and Variable Partitioning.
  - Paging and Segmentation concepts.
- **File Systems**:
  - File attributes, file operations, file access methods (Sequential, Direct).
  - File system structure and directory organization.

## What I Understand
- Dual-mode CPU operation (User mode vs Kernel mode) and how system calls trigger hardware interrupts/traps to switch modes securely.
- Difference between a Process (isolated address space, PCB) and a Thread (shared memory space, lightweight execution).
- CPU Scheduling algorithms trade-offs (e.g. FCFS low overhead vs Round Robin responsiveness vs SJF minimal average wait time).
- Race conditions in shared memory access and why atomic operations / synchronization mechanisms are mandatory.
- The 4 Deadlock conditions and how circular wait causes process starvation.

## What I Can Do
- Explain core OS concepts: processes, threads, memory paging, CPU scheduling, and system calls.
- Analyze CPU scheduling timelines for basic workloads.
- Identify potential race conditions and deadlock risks in concurrent execution flows.

## What I Cannot Yet Do
- Implement OS Kernel modules, custom device drivers, or custom CPU schedulers.
- Debug low-level kernel panics, core dumps, or C memory corruption issues.
- Configure advanced kernel tuning parameters (`sysctl`, kernel memory page allocation, swapiness tuning).

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-005** — Nguyên lý hệ điều hành (TITV) | URL: https://titv.vn/courses-page/he-dieu-hanh/ | Lessons 01-16 (System Calls, CPU Scheduling, Synchronization, Deadlock, Memory Paging)

Master Sources Catalog: [`00-sources/learning-sources.md`](file:///e:/myKnownlage/00-sources/learning-sources.md)

## Weaknesses
- Purely theoretical understanding of OS concepts without writing C kernel/system code.
- Limited deep dive into Virtual Memory (Page fault handling, TLB, Page replacement algorithms like LRU/FIFO).

## Missing Knowledge
- Virtual Memory detail: Page Replacement Algorithms (LRU, Optimal, Clock algorithm), Translation Lookaside Buffer (TLB).
- Storage Management: Disk scheduling algorithms (FCFS, SSTF, SCAN, C-SCAN).
- System Programming in C (`fork()`, `exec()`, `wait()`, POSIX threads `pthread`).

## Recommended Supplement
1. Perform POSIX C system programming labs (`fork()`, `exec()`, `pipe()`, `pthread`, `sem_wait()`).
2. Study Virtual Memory page replacement algorithms in detail.
