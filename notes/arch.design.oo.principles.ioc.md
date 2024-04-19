---
id: pomnv6g69gvwkkw5lbvtcd9
title: Inversion of Control
desc: ''
updated: 1708272212706
created: 1708272168945
---


- IoC inverts the flow of control as compared to traditional control flow.
- A software architecture with this design inverts control as compared to traditional procedural programming
- Normally, what happens is your application code does most of the work and you might use certain libraries to add extra functionality. Or your class is dependent upon other classes to get the job done.

In case of IoC, the framework handles most of the jobs and you focus on just the specific implementation of your application.

## Benefits

As mentioned, one of the benefits is you focus on just your specific logic and implementation and you let the framework handle the trivial stuff like creating an object, allocating memory etc.

It also allows us to depend more on abstraction rather than concrete implementations which in turn promotes:

- loosely coupled architecture
- Flexibility
- plugability

## References

[Ryan Schachte - Dependency Injection & Inversion of Control - YouTube](https://www.youtube.com/watch?v=EPv9-cHEmQw&t=92s)
