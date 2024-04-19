---
id: a9b5rqkkhbtp7zg13oqr3m5
title: Abstraction
desc: ''
updated: 1708252439875
created: 1708240727279
---

Process of hiding implementation details and showing only functionality to user.

## Implemented by

[[paradigm.oo.components.types.abstract]] components like
[[paradigm.oo.components.interface]]s and [[paradigm.oo.components.types.abstract.class]]es.

### How do interface and Abstract class achieve abstraction?

If you're returning an object through an API, you simply pass them an object of the interface, not the class.

The class(implementation) is useless information, the interface is all the consumer will need.

## References

- [Stack Overflow - How abstract class and interface achieve abstraction in java?](https://stackoverflow.com/questions/62646660/how-abstract-class-and-interface-achieve-abstraction-in-java)
  > Typically, the approach is that you only show the user the interface of the object you're passing back to them, instead of the precise class that implements that interface. The interface is the essential implementation, the exact class is unnecessary information.

