---
id: 2z8xdm9vq3jixhezvm672rd
title: Static in Java
desc: ''
updated: 1712933182605
created: 1712932950172
---

## Example of class containing static members

```java
public class Example
{
int x; // Instance variable
static int y; // Static member variable

public void fun() { static int a; } // Instance member function
public static void fun2() { } // Static member function 

static class Test //Static inner class
{ }
}
```

## [[paradigm.oo.components.types.static.variable]]s

- Initialization

    Values can be assigned in special static initializer blocks / [[lang.java.paradigms.oo.instantiation.static blocks]]

- Accessing

    Accessing outside class - `ClassName.VariableName`

- Naming

    When declaring class variables as public static final, then variable names (constants) are all in upper case. If the static variables are not final, the naming syntax is the same as instance and local variables.

## [[lang.java.paradigms.oo.instantiation.static blocks]]

## [[paradigm.oo.components.types.static.method]]s

## Static class

[[lang.java.paradigms.oo.inner class.static]]
