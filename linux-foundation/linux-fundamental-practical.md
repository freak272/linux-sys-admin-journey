# Linux Fundamentals – Practical Application

## Objective

This document demonstrates practical interaction with the Linux system, showing how commands relate to core concepts such as the kernel, system calls, processes, and the filesystem.

---

## 1. Interacting with the Filesystem

### Task: Exploring System Directories

**Commands Used**

```bash
ls /
cd /etc
ls
cd /var/log
ls
```

**Explanation**

* `ls /` lists top-level directories defined by the filesystem structure
* `cd /etc` navigates to system configuration files
* `cd /var/log` accesses system logs

This relates to Linux theory because:

* The filesystem is organized in a structured hierarchy
* Directories like `/etc` and `/var/log` have specific roles
* The kernel manages access to these files and directories

---

## 2. Understanding Processes and CPU Management

### Task: Viewing Running Processes

**Commands Used**

```bash
ps aux
top
```

**Explanation**

* `ps aux` shows all running processes
* `top` displays real-time CPU and memory usage

This demonstrates:

* The kernel is actively scheduling processes
* Multiple processes run concurrently (multitasking)
* CPU time is shared between processes

---

## 3. Memory Management

### Task: Checking Memory Usage

**Commands Used**

```bash
free -h
```

**Explanation**

* Displays total, used, and available memory

This connects to theory:

* The kernel allocates memory to processes
* Memory is managed and isolated to prevent interference

---

## 4. Reading System Information

### Task: Viewing System Files

**Commands Used**

```bash
cat /etc/passwd
```

**Explanation**

* Displays user account information stored in the system

This shows:

* Files store important system data
* The kernel controls access to these files
* Users and processes rely on structured system files

---

## 5. Understanding System Calls (Conceptual Demonstration)

### Task: Running a Simple Command

**Command Used**

```bash
ls
```

**What Happens Internally**

1. User types `ls` in the shell
2. The shell interprets the command
3. The command triggers system calls
4. The kernel processes the request
5. The filesystem is accessed
6. Output is returned to the terminal

**Explanation**

This demonstrates:

* Programs do not access hardware directly
* The kernel acts as the intermediary
* System calls are the bridge between user space and kernel space

---

## 6. Basic Process Control

### Task: Managing a Process

**Commands Used**

```bash
sleep 1000 &
ps aux | grep sleep
kill <PID>
```

**Explanation**

* `sleep 1000 &` runs a process in the background
* `ps aux | grep sleep` finds the process
* `kill` terminates it

This demonstrates:

* Process creation and termination
* The kernel tracks and manages processes
* Users can control processes through commands

---

## 7. Real-World Scenario

### Scenario: Investigating a Slow System

**Steps Taken**

1. Check running processes:

```bash
top
```

2. Identify high CPU usage processes

3. Verify process details:

```bash
ps aux | grep <process_name>
```

4. Stop the process if necessary:

```bash
kill <PID>
```

**Explanation**

This scenario demonstrates:

* CPU management by the kernel
* Process monitoring and control
* Practical troubleshooting using system tools

---

## Summary

This document demonstrates how Linux commands interact with core system concepts:

* Filesystem navigation reflects system structure
* Process commands reveal kernel scheduling
* Memory tools show resource allocation
* System calls connect user commands to kernel operations

These practical examples reinforce the theoretical understanding of how Linux operates internally.
