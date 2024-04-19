---
id: u0zr5crns1nqpfb1uuisw6i
title: Abstract Class
desc: ''
updated: 1708265520458
created: 1708252825421
---

[[paradigm.oo.components.types.abstract.class]]es are mostly used in one of two ways - 

- [[arch.design.oo.use cases for.abstract class.providing flexible behavior for related classes]]: If classes you extend have many common methods and fields, we tend.
- [[arch.design.oo.use cases for.abstract class.helper]]: You want to share code among several closely related classes

Both these ways are better off substituted and hence an **abstract class should almost never be used** since you should try to prefer [[arch.design.oo.principles.composition over inheritance]].

However, this is still a principle and [[philosophy.a principle in principle]].

Some other scenarios where Abstract class may be used:

- The classes you extend require methods with **access modifiers** other than public.
- You want to declare **non-static or non-final fields**. This allows you to define methods that can access and modify the state of the object to which they belong.

You can still consider the above scenarios or use [[arch.design.oo.use cases for.abstract class.stepping stone]].

## References


- [Stack Overflow](https://stackoverflow.com/questions/20193091/recommendations-for-abstract-classes-vs-interfaces#:~:text=If%20you%20are%20designing%20small,component%2C%20use%20an%20abstract%20class.)
    > If we are designing small, concise bits of functionality, use interfaces. If we are designing large functional units, use an abstract class.

- [Nigel Thorne's answer to How to Unit Test Abstract Classes?](https://stackoverflow.com/a/2947823/14318926)
