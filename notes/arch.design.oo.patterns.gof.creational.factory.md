---
id: iu2z450xi9ilzkfir7gxbp0
title: Factory
desc: ''
updated: 1708454509304
created: 1708449293938
---

## Goal
  - Classes of more abstract levels shall not depend on classes on more detailed levels
  - Classes shall only depend on abstractions, e.g. interfaces

## Solution

Move creation of objects to object factory class.

## Object Factory 

- The single responsibility of an object factory class is to create objects of other classes
- The factory decides if it provides the [[arch.design.oo.patterns.gof.creational.singleton]] or a new object every time
- To prevent unwanted side effects due to the direct creation of the managed classes,

```abap
CLASS cl_managed DEFINITION
    PUBLIC
    CREATE PRIVATE "Define the constructor of the factory-managed class as private
    GLOBAL FRIENDS cl_factory "Declare the factory as a global friend of the factory-managed class
```

### Factory using [[paradigm.oo.components.class.friend]]

- Many programming languages support friend classes
- Friend class has access to the class's private constructor and hence can contain the factory method.


## Testability advantage

Offers a single point of injection for [[Test Double]]s in unit tests and integration/system tests

- Create the Interface and multiple implementation of same interface.
- Factory method - used to hide the logic of object creation  - loose coupling and high cohesion
- Create another class and initialize the object in a method over there. Return the object.
