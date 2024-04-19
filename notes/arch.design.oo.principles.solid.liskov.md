---
id: s2xt1e699yr3xkjtcybok86
title: Liskov Substitution Principle
desc: ''
updated: 1708266519440
created: 1708266505393
---

> If B is a subtype of A, then objects of type A may be replaced with objects of type B (i.e., an object of type A may be substituted with any object of a subtype B) without altering any of the desirable properties of the program (correctness, task performed, etc.)

- For instance, if the type Cat is a subtype of Animal, then an expression of type Cat should be substitutable wherever an expression of type Animal is used.
  - **Behavior**
    Animal walks on four legs.
    Cat walks on four legs.
  - **Attribute**
    Animal has two eyes.
    Cat has two eyes.
