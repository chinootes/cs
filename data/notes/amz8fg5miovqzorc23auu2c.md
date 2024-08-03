
> Har thread ka ek stack. Har method ka ek stack frame.

- Used for [[dev.memory management.alloc.static]].
- Used for local variables, function call frames, static thangs, with short lifespan.
- Limited size, more predictable.
- Automatically managed by OS
- Has [[execution.concurrency.multithreading.thread safety]] - Each thread has its own stack.

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

Be careful of [[dev.issues.error.stack overflow]] though.