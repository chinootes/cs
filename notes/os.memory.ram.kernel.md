---
id: 91m29lk3t0d8wamelw4yu43
title: Kernel Space
desc: ''
updated: 1713819009893
created: 1713818933744
---

- Higher part of the virtual memory address space.
- Contains the operating system kernel and its components (such as device drivers, file systems, and process management).
- Not directly accessible from a user process.
- Kernel code and data structures reside here.
- Handles privileged operations (e.g., hardware access, memory management, scheduling).
- Provides services to user processes via syscalls.
- Kernel stack is part of the kernel space and is used for handling interrupts and exceptions.