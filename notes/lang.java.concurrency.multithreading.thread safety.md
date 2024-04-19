---
id: sna2umv15ruskiu91590dgn
title: Thread Safety
desc: ''
updated: 1713125553172
created: 1713125526427
---

How to make a block of code thread safe?

1. Stateless Implementation
    - Source of error in most cases (multithreaded apps)
        - Incorrectly sharing state between several threads
        - Don't make your methods rely on external state, nor maintain any state at all
2. Immutable Implementation
    - Need to share states between threads → make them immutable
    - Immutable classes = Thread safe
3. Thread local fields

    Defining private fields in Thread classes

    - Assigning ThreadLocal instances to a field

        Like normal class fields but each thread accesses them via a setter-getter and gets independently initialized copy of the field so that each thread has its own state

4. Synchronized Collections
5. Concurrent Collections

    Concurrent collections achieve thread safety by dividing their data into segments and acquiring locks on different segments.

    Better performance

6. Atomic objects
7. Synchronized Methods
8. Synchronized statements
9. Other objects as lock
10. Volatile fields
11. Reentrant locks
12. Read/write locks

### Volatile and Atomic 

`volatile` is used when there are two threads store and perform operations on same variable. In such case, both threads store the variable in different caches. This results in inaccuracy and inconsistency. Thus, the `volatile` keyword lets [[lang.java.jre.jvm]] know that this is variable is going to be changed and it is then stored in the common cache.

`AtomicInteger`, `AtomicLong` and other such classes are used in a similar situation to above, where the threads are accessing and performing some operation on a variable. If we don't define the variable as Atomic, it might happen that the second thread accesses the variable before the first thread is done performing operation on it. This causes inconsistency in the data. The `AtomicInteger` makes the integer thread safe by not letting any other thread access until one thread is done.
