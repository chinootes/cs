---
id: s8w6h8osx1d6r15k29phief
title: Generational
desc: ''
updated: 1713687650282
created: 1713686886387
---

Garbage collection is performed on objects on basis of their age in the program.

### Heap Memory Division

Generational garbage collector divides the heap memory into different generations based on the lifespan of objects.

Heap is divided into:

- Young Generation (Eden Space)
- Old Generation
- Survivor space 
    - 1
    - 2

#### Garbage collection life cycle

- Objects are stored in Eden space, when they are created at first.
- 1st cycle - When Eden Space gets full
    - Minor GC runs
    - Objects moved to survivor space 1
- Susequent cycles - Eden space gets full again
    - Objects moved to survivor space 2
      from both Eden space and survivor 1

💡 Objects keep moving between both survivor spaces in cycles

Objects older than Max tenure threshold (a certain threshold for number of cycles) are moved to old generation space.

- When old generation space is about to be full
- major GC runs → *time consuming and might pause the application*