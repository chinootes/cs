
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