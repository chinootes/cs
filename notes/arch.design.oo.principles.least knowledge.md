---
id: 5p2u2l4kks65dp3kuf526zy
title: Law of Demeter or Principle of Least Knowledge
desc: ''
updated: 1708779350045
created: 1708779284512
---

> Don't talk to strangers.

## Statement

**For all classes C, and for all methods M attached to C, all objects to which M sends a message must be:**

- **M’s argument objects, including the self object or**
- **The instance variable objects of C**

**(Object created by M, or by functions or methods which M calls, and objects in global variables are considered as arguments of M).**

*In the early days of Object-Orientation, objects were supposed to “send messages” to each other. That is how they communicated. So the term “objects to which M sends a message” roughly translates to “objects used by M,” or in a more practical definition “objects on which M calls a method on”.*

## The Genius of Law of Demeter

- Concepts like encapsulation, cohesion, single-responsibility principle or open/closed principle are not pragmatic enough and require interpretation, which makes them subjective and dependent of people's experience and knowledge.

> The genius of the Law of Demeter comes from the succinct and exact definition, which allows for a direct application when writing code, while at the same time almost automatically guaranteeing proper encapsulation, cohesion, and loose coupling. The authors of the Law managed to take these abstract concepts and distil the essence of them into a clear set of rules that are universally applicable to Object-Oriented code. [[Source](https://dzone.com/articles/the-genius-of-the-law-of-demeter#:~:text=The%20genius%20of%20the%20Law%20of%20Demeter%20comes,that%20are%20universally%20applicable%20to%20Object%2DOriented%20code.)]

## References

[The Genius of Law of Demeter - dZone](https://dzone.com/articles/the-genius-of-the-law-of-demeter)
