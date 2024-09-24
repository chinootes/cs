---
id: lx58207ls3auw10jnxmdcmj
title: Predicate
desc: ''
updated: 1727000143700
created: 1726996519242
---

- [[lang.java.paradigms.func.interface]] which represents a boolean-values function that takes **one** argument.
- Provides a convenient way to define and pass around functions that return a true or false value based on their input.

## Definition

```java
@FunctionalInterface
public interface Predicate<T> {
    boolean test(T t);
}
```

It is also [[Generic|lang.java.typing.generics]].

## Usage

```java
Predicate<String> isEvenLength = s -> s.length() % 2 == 0;
boolean result = isEvenLength.test("Hello");
```