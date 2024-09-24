---
id: vqbisdumti23oeq2xk6oml5
title: String
desc: ''
updated: 1727122318634
created: 1711643845722
---

- **String literal**: A string [[dev.lingo.literal]] in Java is basically a sequence of characters from the source character set. 
- String literals initialised are an object of this String class.

💡 While printing an object, Java compiler implicitly calls toString() method.

## String Memory Management

![[lang.java.jre.memory.string]]

## Immutability

String in Java is an [[arch.design.oo.patterns.immutable class]].


![[arch.design.oo.patterns.immutable class#benefits]]

- String Pooling: Memory management using string pool is only possible because strings are immutable.



## null vs empty String

```java
String getSome;
String getMose = "";
```

Both of them are not the same. `""` is a literal and has a reference pointing to it in the String constant pool, while `getSome` has no value/reference in it so its null → default value for String.
