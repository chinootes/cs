---
id: dkdtvct3q6f8lggmoqrqf43
title: Collection Framework
desc: ''
updated: 1717342998926
created: 1713633121566
---

Java Collection Framework defines several classes and interfaces to represent group of individual objects as single entity, i.e. [[data.structure]].  

Although, referred to as a framework, it functions more like a library with a collection of classes and interfaces.

💡 Every Collection class is based on some standard data structure.

- All Collection Classes implement [[lang.java.lib.interfaces.marker.serializable]] and [[lang.java.lib.interfaces.marker.cloneable]]

    - Why though?

        Collections $\equiv$ Containers in C++ → used to transfer

        To transfer object from one place to another, it should be **serializable**.

        When sent from one place to another, the receiver makes a copy of it and operates on it → **clonable**

 
 ## References

 - [Collections Framework Overview - Java - Oracle Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/overview.html#:~:text=Not%2C%20strictly%20speaking%2C%20a%20part%20of%20the%20collections,and%20relies%20on%20some%20of%20the%20same%20infrastructure.)