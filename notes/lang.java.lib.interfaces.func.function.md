---
id: gfq63atn6koxm8w8u1nb38b
title: Function
desc: ''
updated: 1727001256344
created: 1727000678991
---

- Represents a function that takes one argument and produces one result. 
- Used for expressing computations and transformations.


## Definition

```java
@FunctionalInterface
public interface Function<T, R> {
    R apply(T t);
}
```
T - input type
R - output type


## Usage

```java
Function<String, Integer> stringLength = s -> s.length();
int lengthOfHello = stringLength.apply("Hello"); // 5
```