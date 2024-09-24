---
id: ae0jf8mu7bgpgcnnmf9c9vd
title: Consumer
desc: ''
updated: 1727012479897
created: 1727012365791
---

Represents an action that takes in a single input and returns no result.

## Definition

```java
@FunctionalInterface
public interface Consumer<T> {
    void accept(T t);
}
```