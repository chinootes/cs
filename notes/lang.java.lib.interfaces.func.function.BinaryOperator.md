---
id: bqk8yqp4sz0wza0da1rnpru
title: BinaryOperator
desc: ''
updated: 1727013284746
created: 1727013153565
---

- Takes two inputs and returns one - all of the same type.
- Great for performing binary operations on objects like 2+5=7

## Definition

```java
@FunctionalInterface
public interface BinaryOperator<T> {
    T apply(T t, T u);
}
```


## Usage

```java
BinaryOperator<Integer> sum = (x, y) -> x + y;
int result = sum.apply(5, 3); // 8
```