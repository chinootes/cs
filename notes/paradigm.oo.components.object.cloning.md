---
id: n7u2e2qciuveu0n4obbblqd
title: Object Cloning
desc: ''
updated: 1708401406810
created: 1708401391429
---

## Shallow Cloning

```java
A obj = new A();
obj.i = 5;
obj.j = 6;

A obj1 = obj; //Shallow cloning
```

The object is only one. We have just created two references to the same object.

## Deep Cloning

```java
A obj1 = new A();
obj1.i = obj.i;  //Deep
obj1.j = obj.j;  //Cloning
```

- We create a new object and manually copy all members one by one.
- Not very efficient if there are too many data members.
