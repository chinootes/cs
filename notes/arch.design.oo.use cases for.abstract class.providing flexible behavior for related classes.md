---
id: xbbmh059cyr58w5l55kihjo
title: Abstract Class for Providing Flexible Behavior for Related Classes
desc: ''
updated: 1708262876997
created: 1708254610218
---

If there is a common interface for all concrete implmentations of your abstract class, it means you are just using [[paradigm.oo.pillars.inheritance]] to define/change certain behaviour of the class.

```mermaid
classDiagram
  iCar <|-- AbstractCar
  AbstractCar <|-- GoCart
  AbstractCar <|-- FastCar  
```

You should rather prefer [[arch.design.oo.principles.composition over inheritance]].

Just turn your abstract class into a concrete implementation and inject the "behaviour" which you are trying to change from outside using [[arch.design.oo.patterns.gof.behavioural.strategy]].

```mermaid
classDiagram
  iCar <-- Car
  class Car{
    + iMotor motor
  }
  iMotor <-- FastMotor
  iMotor <-- GoCartMotor  
```

## References

[Nigel Thorne's answer to How to Unit Test Abstract Classes?](https://stackoverflow.com/a/2947823/14318926)
