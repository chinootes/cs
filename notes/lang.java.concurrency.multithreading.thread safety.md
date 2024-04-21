---
id: sna2umv15ruskiu91590dgn
title: Thread Safety
desc: ''
updated: 1713648544553
created: 1713125526427
---

How to make a block of code thread safe?

In addition to the usual ways to ensure [[execution.concurrency.multithreading.thread safety]], Java provides some additional [[execution.concurrency.synchronization]] mechanisms:

1. Thread local fields

    Defining private fields in Thread classes

    - Assigning ThreadLocal instances to a field

        Like normal class fields but each thread accesses them via a setter-getter and gets independently initialized copy of the field so that each thread has its own state

2. Synchronized Collections
3. Concurrent Collections

    Concurrent collections achieve thread safety by dividing their data into segments and acquiring locks on different segments.

    Better performance

4. Atomic objects
5. Synchronized Methods
6. Synchronized statements
7. Other objects as lock
8. Volatile fields
9. Reentrant locks
10. Read/write locks

### Volatile and Atomic 

`volatile` is used when there are two threads store and perform operations on same variable. In such case, both threads store the variable in different caches. This results in inaccuracy and inconsistency. Thus, the `volatile` keyword lets [[lang.java.jre.jvm]] know that this is variable is going to be changed and it is then stored in the common cache.

`AtomicInteger`, `AtomicLong` and other such classes are used in a similar situation to above, where the threads are accessing and performing some operation on a variable. If we don't define the variable as Atomic, it might happen that the second thread accesses the variable before the first thread is done performing operation on it. This causes inconsistency in the data. The `AtomicInteger` makes the integer thread safe by not letting any other thread access until one thread is done.
