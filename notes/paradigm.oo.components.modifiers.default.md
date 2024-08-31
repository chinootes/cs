---
id: 47krk218fjo475qgehvmlj3
title: Default
desc: ''
updated: 1725005938488
created: 1725004741719
---

Default modifer, used for **methods**, helps define default implementations to certain methods within the interface itself.

The primary purpose for this feature is to allow adding certain default behaviour to future versions of an interface without breaking the existing functionality and supporting backward compatibility.

This is not present in all OO languages though.


```java

public interface MyInterface {
    void existingMethod(); // Abstract method

    // Default method with implementation
    default void newDefaultMethod() {
        System.out.println("This is a default method.");
    }
}
```