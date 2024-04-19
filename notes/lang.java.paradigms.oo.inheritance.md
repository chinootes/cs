---
id: bch7o33cdf951wavbv1ob6p
title: Inheritance
desc: ''
updated: 1712932627101
created: 1712930362832
---

- Implemented by

    extends keyword

## Types of Inheritance in Java

- [[paradigm.oo.pillars.inheritance.types.single]]
- [[paradigm.oo.pillars.inheritance.types.multilevel]]
- [[paradigm.oo.pillars.inheritance.types.hierarchical]]
- [[paradigm.oo.pillars.inheritance.types.hybrid]]

[[paradigm.oo.pillars.inheritance.types.multiple.not allowed]]


## Inheritance in case of [[lang.java.paradigms.oo.encapsulation.access.default]]

- Are fields and methods with `default` access inherited?

    Only if the subclass is located in the same package as the superclass.

- How is multiple inheritance handled in case of methods with `default` access?

    In case both parent interfaces have a default method with same method signature, the implementing class should explicitly tell which one its trying to use or it should override the default method.

    ```java
    //If I1 and I2 both have a fun() as default method
    class C implements I1, I2{
    I1.super.fun(); //Use I1's fun() method
    }
    ```
