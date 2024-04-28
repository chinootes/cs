---
id: do8sqp0l9edsmgdg7ktdho0
title: Heap Space
desc: ''
updated: 1713809701127
created: 1713805253604
---

- For objects and data structures with longer lifespan.
- Not [[execution.process.thread]]-specific. All threads can access it.
- Heap memory can lead to memory leaks.
- Bigger than [[arch.design.memory management.spaces.stack]]
- Can have [[arch.design.memory management.manual]] or [[arch.design.memory management.implicit]] depending upon the implementation. But even an implicit memory management strategy needs to have an entity ([[arch.design.memory management.implicit.gc]]) cleaning up the data.
- Prone to [[arch.design.memory management.leaks]]