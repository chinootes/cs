---
id: 7y06se6mdlgmuptqgjdn5kq
title: Disadvantages of Composition
desc: ''
updated: 1708265844048
created: 1708261398271
---

1. You can't change the implementation provided by superclass at runtime. Inheritance is defined at compile time.
2. Inheritance is said to "break encapsulation" by exposing a subclass to protected members of parent class
3. Leads to child class being tightly coupled with parent class. Changes in parent class will lead to changes in subclass.
4. Excessive deep inheritance trees can make inheritance stack very deep and confusing.

## References

[Prefer composition over inheritance? - Stack Overflow](https://stackoverflow.com/questions/49002/prefer-composition-over-inheritance)
