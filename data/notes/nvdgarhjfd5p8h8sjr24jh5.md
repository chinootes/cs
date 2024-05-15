

- Implemented by

    extends keyword

## Types of Inheritance in Java

- [[paradigm.oo.principles.inheritance.types.single]]
- [[paradigm.oo.principles.inheritance.types.multilevel]]
- [[paradigm.oo.principles.inheritance.types.hierarchical]]
- [[paradigm.oo.principles.inheritance.types.hybrid]]

[[paradigm.oo.principles.inheritance.types.multiple.not allowed]]


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
