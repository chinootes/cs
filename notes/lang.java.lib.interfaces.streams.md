---
id: baxu095ehryiz9aqa17tpvt
title: Streams
desc: ''
updated: 1725466274887
created: 1725014887363
---

Framework for processing sequences of data in declarative and functional style.

Basically, you can specify an operation and perform it for all items in the collection.


## Operations

### Intermediate Operations

- `filter(Predicate)`: 
- `map(Function)`: 
- `flatMap(Function)`: 
- `distinct()`:
- `sorted()`:
- `sorted(Comparator)`:
- `peek(Consumer)`:
- `limit(long n)`:
- `skip(long n)`:


### Terminal Operations

- `forEach(Consumer)`
- `collect(Collector)`
- `reduce(BinaryOperator)`
- `toArray()`
- `min(Comparator)`
- `max(Comparator)`
- `count()` 
- `anyMatch(Predicate)`
- `allMatch(Predicate)`
- `noneMatch(Predicate)`
- `findFirst()`
- `findAny()` 