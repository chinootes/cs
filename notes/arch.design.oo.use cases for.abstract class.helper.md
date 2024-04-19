---
id: zkmonp4k5pfdtnwlya8ybo5
title: Abstract Class as a Helper Class
desc: ''
updated: 1708263243591
created: 1708254698813
---

If you have different interfaces for the child classes, but you are using the abstract class to factor out duplication within objects, then your abstract class is working as a base class.

```mermaid
classDiagram
    AbstractBaseThingWithMotor <-- LawnMower
    AbstractBaseThingWithMotor <-- Car    
```

See if this functionality can be moved to a concrete helper class instead.

```mermaid
classDiagram
    class LawnMower{
        + iMotorHelper motorHelper
    }
    class Car{
        + iMotorHelper motorHelper
    }    
    iMotorHelper <-- MotorHelper
```

## References

[Nigel Thorne's answer to How to Unit Test Abstract Classes?](https://stackoverflow.com/a/2947823/14318926)
