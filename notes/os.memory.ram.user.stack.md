---
id: amz8fg5miovqzorc23auu2c
title: Stack Space
desc: ''
updated: 1713820120476
created: 1713805011532
---

> Har thread ka ek stack. Har method ka ek stack frame.

- Used for [[programming.memory management.alloc.static]].
- Used for local variables, function call frames, static thangs, with short lifespan.
- Limited size, more predictable.
- Automatically managed by OS
- Has [[execution.concurrency.multithreading.thread safety]] - Each thread has its own stack.
- Stack grows downward to lower addresses.

## Stack allocation

This is controlled by the OS. One stack is allocated to the program for each running thread.

### Stack Size Estimation

- The OS allocates a stack for each system-level thread when the thread is created.
- The size of the stack is typically determined by the OS and compiler settings.
- For instance, on many systems, the default stack size might be around 1 MB to 2 MB.
- This default size is generally sufficient for most routine operations and function calls.


### Dynamic Allocation and Swapping


- Some systems can automatically grow the stack if there’s room in the virtual address space.


### Customization

While the OS provides a default stack size, some applications or languages allow customization. Developers can adjust the stack size based on their specific requirements.

Be careful of [[programming.issues.error.stack overflow]] though.

## Why choose [[data.structure.secondary.stack]] for this purpose?

The design decision by OS Gods to choose this data structure to represent this memory space comes from the below reasoning.

Each function call creates a new [[os.memory.ram.user.stack.frame]] on the stack, containing local variables, return addresses, and other bookkeeping information.

The LIFO (last in, first out) structure of the stack ensures that function calls are properly nested and managed.