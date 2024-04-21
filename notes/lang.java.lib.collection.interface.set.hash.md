---
id: eefrdgpwwtmz7fliwvlgs8u
title: HashSet
desc: ''
updated: 1713647142863
created: 1713639311903
---

implements [[lang.java.lib.collection.interface.set]]

- Underlying Data Structure: [[data.structure.secondary.hash.table]]
- [[lang.java.lib.collection.tags.duplicates.not allowed]]
- [[lang.java.lib.collection.tags.insertion order.not preserved]] (in order of hashcode)
- [[lang.java.lib.collection.tags.null insertion.not allowed]]
- Best choice for: Search Operations
- Worst choice for:
- Constructors:
  1. `HashSet h = new HashSet();`
  2. `HashSet h = new HashSet(int initialCapacity)`
  3. `HashSet h = new HashSet(int initialCapacity, float loadFactor)`
  4. `HashSet h = new HashSet(Collection C)`
- Default initial capacity: 16
- Load factor/fill ratio: 0.75
- New Capacity:

- What will happen if we try to enter duplicate value for set?
    add() method will return false.
    👆🏽 return type is boolean

- Insertion order
    Object stored in order of hashcode()
    👆🏽 Makes it best choice for search operations

Child classes/interfaces:

[[lang.java.lib.collection.interface.set.hash.linked]]
