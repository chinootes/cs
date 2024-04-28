---
id: amz8fg5miovqzorc23auu2c
title: Stack Space
desc: ''
updated: 1713805971427
created: 1713805011532
---

- Used for [[arch.design.memory management.alloc.static]].
- Used for local variables, function call frames, static thangs, with short lifespan.
- Limited size, more predictable.
- Automatically managed
- Has [[execution.concurrency.multithreading.thread safety]] - Each thread has its own stack.
