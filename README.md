# Operating Systems - Laboratory

![Platform](https://img.shields.io/badge/Platform-Ubuntu%20Linux-E95420?logo=ubuntu&logoColor=white)
![Language](https://img.shields.io/badge/Language-C-A8B9CC?logo=c&logoColor=black)
![Compiler](https://img.shields.io/badge/Compiler-GCC-blue)
![API](https://img.shields.io/badge/API-POSIX%20Threads%20(pthread)-lightgrey)

## Overview
This repository contains the complete submission for the **Operating Systems - Laboratory** assignment from the **Department of Software Engineering, University of Business and Technology (UBT)**. 

The assignment covers core operating system concepts, Linux command-line operations, system-level C programming on Ubuntu Linux, and classic resource management and scheduling algorithms.

---

## Repository Contents

* **`Operating Systems - Laboratory.pdf`** — Complete laboratory report containing theoretical answers, C source code, algorithm step-by-step calculations, Gantt charts, and execution screenshots.
* **Screenshots** — Terminal execution captures from Ubuntu Linux demonstrating shell commands, `fork()` process management, `pthread` mutex synchronization, and CPU scheduling tables.

---

## Topics & Solutions Covered

### Part 1: Operating System Fundamentals & Process Management
| Question | Topic | Summary of Implementation & Concepts |
| :--- | :--- | :--- |
| **Q1** | **OS Fundamentals** | Role of the OS as a resource allocator and control program; distinction between the kernel and command-line shell. |
| **Q2** | **Virtualization** | Host OS vs. Guest OS architecture and the role of Oracle VirtualBox as a Virtual Machine Manager (VMM). |
| **Q3** | **Linux Commands** | Executed `pwd`, `mkdir SE418`, `ls -a`, and `ps` in the Ubuntu Bash terminal. |
| **Q4** | **Process Management (C)** | Implemented `fork_demo.c` using `fork()`, `getpid()`, and `wait()` to synchronize parent and child processes. |
| **Q5** | **OS Security** | Analysis of unauthorized access and privilege escalation; resource protection using Linux UIDs, GIDs, `chmod`, `umask`, and `chown`. |

### Part 2: Operating System Algorithms & Resource Management
| Question | Topic | Key Results & Takeaways |
| :--- | :--- | :--- |
| **Q6** | **CPU Scheduling** | Compared **FCFS** (Avg. Waiting Time: `3.33 ms`) vs. **Non-preemptive SJF** (Avg. Waiting Time: `3.00 ms`) with Gantt charts. |
| **Q7** | **Multithreading & Sync (C)** | Implemented `q7_threads.c` using POSIX Threads (`pthread`) and `pthread_mutex_t` to prevent race conditions on a shared counter. |
| **Q8** | **Banker's Algorithm** | Calculated the `Need` matrix (`Max - Allocation`), verified a **Safe State**, and identified the safe sequence `<P2, P0, P1>`. |
| **Q9** | **Memory Allocation** | Evaluated **First Fit**, **Best Fit**, and **Worst Fit**; **Best Fit** achieved optimal memory utilization (`1167 KB` allocated). |
| **Q10** | **Page Replacement** | Traced a 13-page reference string across 3 frames: **Optimal** (`7` faults) outperformed **LRU** (`9` faults) and **FIFO** (`10` faults). |

---

## Environment & Compilation Setup

All programming tasks were written, compiled, and tested on **Ubuntu Linux** using the **GCC** compiler:

* **Process Creation (`Q4`):**
  ```bash
  gcc fork_demo.c -o fork_demo
  ./fork_demo
