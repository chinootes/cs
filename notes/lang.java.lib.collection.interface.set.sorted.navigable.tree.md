---
id: n0bs3k84v4lefk1bk9j656s
title: TreeSet
desc: ''
updated: 1713644494113
created: 1713641118537
---

# TreeSet

implements [[lang.java.lib.collection.interface.set.sorted.navigable]]

- Underlying Data Structure: Balanced Tree
- [[lang.java.lib.collection.tags.duplicates.not allowed]]
- [[lang.java.lib.collection.tags.insertion order.not preserved]]
- [[lang.java.lib.collection.tags.null insertion.not allowed]]
- [[lang.java.lib.collection.tags.heterogeneous objects.not allowed]]
- Best choice for: Cache-based application
- Worst choice for:
- Constructors:
  1. `TreeSet A = new TreeSet()`
  2. `TreeSet A = new TreeSet(Comparator C)`
  3. `TreeSet A = new TreeSet(Collection C)`
  4. `TreeSet A = new  TreeSet(SortedSet S)`
- Default initial capacity: 0
- Load factor/fill ratio:
- New Capacity: Increases as elements are added
