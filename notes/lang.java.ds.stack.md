---
id: lubjpq6xfglfx03cmfbdfoc
title: Stack
desc: ''
updated: 1714652261144
created: 1714651062267
---

[[lang.java.lib.collection.interface.list.vector.stack]] class can be used.

## Creating

```java
Stack<Integer> stack = new Stack<>();
```

## Pushing

```java
stack.push(i)
```

## Popping

```java
Integer i = stack.pop()
```

## Peeking

Returns last element without removing.

```java
Integer i = stack.peek()
```

## Searching

Returns position of the element. 

Position starts from 1(not 0) and is counted from the topmost(last) element.

Returns -1 if element is not found.

```java
Integer pos = stack.search(element);
```
