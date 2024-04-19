---
id: tla9lmgojyihaq18m4gxgqe
title: String
desc: ''
updated: 1712859993775
created: 1711643845722
---

- **String literal**: A string literal in Java is basically a sequence of characters from the source character set.
- String in Java is an [[arch.design.oo.patterns.immutable class]]
- String literals initialised are an object of this String class.

💡 While printing an object, Java compiler implicitly calls toString() method.


# null vs empty String

```java
String getSome;
String getMose = "";
```

Both of them are not the same. `""` is a literal and has a reference pointing to it in the String constant pool, while `getSome` has no value/reference in it so its null → default value for String.