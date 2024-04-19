---
id: c1ss03qpecs4uh8mdqeqv7v
title: Object Cloning in Java
desc: ''
updated: 1712939500761
created: 1712939265697
---


The usual [[paradigm.oo.components.object.cloning]] ways work just as well in Java. However, clone() method is much easier and can be used to overcome the limitations of those methods.

```java
A obj1 = (A) obj.clone();
```


`clone` is a member function of [[Object]] which throws an exception when used. Why?

Cloning a class is [[tags.not allowed by default]] for security reasons. But if the class itself allows you i.e. the class implements Cloneable [[lang.java.lib.interfaces.marker]], then you can use `clone()` method.

