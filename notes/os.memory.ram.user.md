---
id: rfzgs3wdwjshx6akw104ec5
title: User Space
desc: ''
updated: 1713818588690
created: 1713818447834
---

Portion of a process’s virtual memory address space that is accessible to user-level applications.

Contains data, code, stack, and heap specific to the user process.
User programs execute in this space.

User , while dynamic allocations (
User space is isolated from other processes.
User applications interact with the kernel through system calls (syscalls) when they need restricted services.