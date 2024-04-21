---
id: hf45oxhpq9ii2ujvaqnitdz
title: SortedSet
desc: ''
updated: 1713641063064
created: 1713640721490
---
# SortedSet

implements [[lang.java.lib.collection.interface.set]]

- [[lang.java.lib.collection.tags.duplicates.not allowed]]
- [[lang.java.lib.collection.tags.insertion order.preserved]]
- Sorting Order: Customizable

| Methods |Returns |
|-----------|---------------|
| `first()` | first element |
| `last()`  | last element  |
| `headSet(a)` | elements less than *a*  |
| `tailSet(a)` | elements greater than or equal to *a* |
| `subSet(a,b)` | elements between *a* and *b* including *a* |
| `comparator()` | Comparator object which defines underlying sorting technique  |
|                   |   (If we're using default natural sorting order, then it simply returns null) |


Child classes/interfaces:

[[lang.java.lib.collection.interface.set.sorted.navigable]] (I)
