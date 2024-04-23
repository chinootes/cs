---
id: ebrkz8wg3nundlii209591y
title: Garbage collection
desc: ''
updated: 1713844725899
created: 1713685879545
---

- Garbage collection (GC) is a process that reclaims unused memory during program execution.
- When a program allocates memory for objects (such as variables, data structures, or objects created dynamically), some of that memory may become unreachable (i.e., no longer referenced by any part of the program).
- The garbage collector identifies and frees up this unreferenced memory, making it available for future allocations.


## Does [[programming.memory management.implicit]] really prevent [[programming.memory management.leaks]] from happening?

"No memory leaks" is a common argument given in support of automatic memory management. Although, with languages supporting garbage collection, you are leaking memory constantly. Since, you are allocating memory (you have some control there at least), but the language forces you to forget about the allocated memory. There always some garbage in the system inherently.

**Why it is bad?**

Although it doesn't necessarily cause much issues in the application itself. The application consumes more memory than necessary, leaving the memory, which could've been utilized by other processes, hogged. 

Garbage collection is a selfish algorithm. As in, it cares only about the application. Unless it works closely with the OS and the OS can ask it to free up some memory, other processes may suffer from shortage of free memory.

## References

- [Why I hate Java - No memory leaks](http://warp.povusers.org/grrr/java.html#:~:text=presented%20defending%20it.-,No%20memory%20leaks%3F,-The%20most%20usual)