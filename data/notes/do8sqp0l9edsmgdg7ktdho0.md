
- For objects and data structures with longer lifespan.
- It is a **dynamic memory pool** provided by the OS which can be allocated and deallocated by the programs. Therefore, the applications have control of the heap memory. It is not managed by OS.
- Not [[execution.process.thread]]-specific. All threads can access it => Not as safe as [[os.memory.ram.spaces.stack]]
- Heap memory can lead to memory leaks.
- Bigger than [[os.memory.ram.spaces.stack]]
- Can have [[dev.memory management.manual]] or [[dev.memory management.implicit]] depending upon the implementation. But even an implicit memory management strategy needs to have an entity ([[dev.memory management.implicit.gc]]) cleaning up the data.
- Prone to [[dev.memory management.leaks]]