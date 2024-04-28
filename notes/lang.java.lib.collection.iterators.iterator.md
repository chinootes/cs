---
id: 35b9rz7t9tkhu0sganracma
title: Iterator
desc: ''
updated: 1713680957261
created: 1713680927280
---

- Applicable for any collection class
- Both read and remove method

## Methods

`public boolean hasNext()`

`public Object next()`

`public void remove()`

## Usage

The Collection interface has a iterator() method which returns an object of Iterator.

public Iterator iterator()

```java
Iterator itr = c.iterator(); //c is any collection object

//Usage similar to Enumeration
```

## Limitations

- Enumeration and Iterator - both are only forward direction cursor
- No method to replace or add new object
