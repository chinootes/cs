---
id: gz94pgtztppo7a4z12wdwv6
title: Reference Variables
desc: ''
updated: 1708612968351
created: 1708611231195
---

- References are strongly typed

    Type of a reference is much more strictly controlled in Java than the type of a [[programming.components.variable.pointer]] is in C. In C you can have an `int*` and cast it to a `char*` and just re-interpret the memory at that location. That re-interpretation doesn’t work in Java: you can only interpret the object at the other end of the reference as something that it already is (i.e. you can cast a Object reference to String reference only if the object pointed to is actually a String).

- References are not memory addresses per se. They are more like object handles.
  - The object's memory address will change when it's moved. But the object handle will stay the same.
  - For example, JVM is allowed to use moving garbage collectors, which means objects can be relocated by the GC. (In fact, generational GCs frequently relocate objects, when migrating them between generations.)
  - [[programming.components.variable.pointer.arithmetic]] nlot allowed.

## References

- [C/C++ Pointers vs Java References](https://www.geeksforgeeks.org/is-there-any-concept-of-pointers-in-java/) — Geeks for geeks
- [If Java uses references and references are just memory addresses, can I perform arithmetic operations on the addresses they point to? — Quora](https://www.quora.com/If-Java-uses-references-and-references-are-just-memory-addresses-can-I-perform-arithmetic-operations-on-the-addresses-they-point-to)
