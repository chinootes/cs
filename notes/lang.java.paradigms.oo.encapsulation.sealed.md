---
id: e7lsiiivoi1kxwt68kc0m0o
title: Sealed Classes
desc: ''
updated: 1714720771137
created: 1714720626416
---

Sealed classes restrict which classes can inherit them, enhancing encapsulation and giving more control.

```java
public abstract sealed class Shape permits Circle, Rectangle {
    // Common methods and fields
}

public final class Circle extends Shape {
    // Circle-specific implementation
}

public final class Rectangle extends Shape {
    // Rectangle-specific implementation
}

```

Introduced in [[lang.java.v.17]].