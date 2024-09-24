---
id: k83mi3ehud8dj1dey48p9iv
title: Memory
desc: ''
updated: 1727121179510
created: 1727079525124
---

JRE's memory is segregated into the below parts:

## Class (Method) Area

Stores class level data of every class such as the runtime constant pool, field and method data, the code for methods.

## Heap Space

Java's [[os.memory.ram.user.heap]] implementation.

Used to allocate memory to objects at run time

### Program Counter Register

- Stores address of currently executing instruction.

    Example: Points to the first line at the start of the program execution

- Also stores address of threads reponsible for executing current instruction
- Size very small
- No effect of Java apps on PC register memory or its content

## Stack

Java's implementation of [[os.memory.ram.user.stack]].

- Each thread has a private JVM stack created at same time as thread
  - Used to store data and partial results which will be needed while returning value for method and performing dynamic linking
- Stores [[os.memory.ram.user.stack.frame]]s
- References to objects stored here

### Stack Frame

- A new frame is created each time at every invocation of the method.
- Contains all the data for one function call - parameters, return address and its local address
- Stack frame destroyed when method execution completes

## Native Method Stack

- Implemented using languages other than Java
- New thread created → Memory allocated in this area
- Size can be fixed or dynamic

## References

- [How references are stored in Java](https://stackoverflow.com/questions/61654407/how-references-are-stored-in-java)
- More about layout of java objects — [Java Objects Inside Out](https://shipilev.net/jvm/objects-inside-out/)
- [Compressed OOPs](https://wiki.openjdk.java.net/display/HotSpot/CompressedOops)