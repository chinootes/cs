
- For objects and data structures with longer lifespan.
- It is a **dynamic memory pool** provided by the OS which can be allocated and deallocated by the programs. Therefore, the applications have control of the heap memory. It is not managed by OS.
- Not [[execution.process.thread]]-specific. All threads can access it => Not as safe as [[os.memory.ram.user.stack]]
- Heap memory can lead to memory leaks.
- Bigger than [[os.memory.ram.user.stack]]
- Needs [[dev.memory management.manual]]. 

    💡 Some virtual machines can provide [[dev.memory management.implicit]]. But even an implicit memory management strategy needs to have an entity ([[dev.memory management.implicit.gc]]) cleaning up the data.

- Heap grow upwards to higher addresses.
- Prone to [[dev.memory management.leaks]]


## Why choose heap data structure for this memory space?

The Heap space doesn't actually adhere to the heap data structure. It is just called so because it is a free store where memory blocks are allocated and deallocated dynamically - like a "heap" of memory blocks.