---
id: tag4ci15orv7zzfhpppsh1t
title: Dependency Injection
desc: ''
updated: 1715105585072
created: 1708275674575
---

```abap
CLASS … DEFINITION … .
 DATA(lo_cash_provider) = NEW cl_cash_provider( ).
ENDCLASS
```

👆🏽 This here is a [[concepts.dependency]]

- Dependency injection is a design pattern in which, instead of creating the object ourselves in our code, we let some other entity create the object and "inject" into our class.
- ⇒ Dependency injection implements [[arch.design.oo.principles.ioc]]

The dependency can be injected via:

- constructor -- [[arch.design.oo.patterns.di.constructor]]
- setter method -- [[arch.design.oo.patterns.di.setter]]
- parameter - [[arch.design.oo.patterns.di.parameter]]
- backdoor - [[arch.design.oo.patterns.di.backdoor]]