---
id: fi3xznhjsf8ezkolih7torp
title: Collection Frameworks Cheatsheet
desc: ''
updated: 1713680858177
created: 1713676509304
---

#Cheatsheet

- All Collection Classes implement [[lang.java.lib.interfaces.marker.serializable]] and [[lang.java.lib.interfaces.marker.cloneable]]
- [[lang.java.lib.collection.tags.heterogeneous objects.allowed]] for all collections except [[lang.java.lib.collection.interface.set.sorted.navigable.tree]] and [[lang.java.lib.collection.map.sorted.navigable.tree]].

## Interface and Class Hierarchy
_I = Interface_
_AC = Abstract Class_
Underlying Data Structure mentioned beside the classes.

💡 Every Collection class is based on some standard data structure.

In order of hierarchy:

- [[lang.java.lib.collection.interface]] (I)
- [[lang.java.lib.collection.interface.list]] (I)
  - [[lang.java.lib.collection.interface.list.array]] - Resizable Array
  - [[lang.java.lib.collection.interface.list.linked]] - Doubly Linked List
  - [[lang.java.lib.collection.interface.list.vector]] - Resizable Array
    - [[lang.java.lib.collection.interface.list.vector.stack]] - Stack
- [[lang.java.lib.collection.interface.set]] (I)
  - [[lang.java.lib.collection.interface.set.hash]] - Hash table
    - [[lang.java.lib.collection.interface.set.hash.linked]] - Hash table
  - [[lang.java.lib.collection.interface.set.sorted]] (I)
    - [[lang.java.lib.collection.interface.set.sorted.navigable]] (I)
      - [[lang.java.lib.collection.interface.set.sorted.navigable.tree]] -  Balanced Tree
- [[lang.java.lib.collection.interface.queue]] (I)
  - [[lang.java.lib.collection.interface.queue.priority]]
  - [[lang.java.lib.collection.interface.queue.blocking]]
    - [[lang.java.lib.collection.interface.queue.blocking.priority]]
    - [[lang.java.lib.collection.interface.queue.blocking.linked]]
- [[lang.java.lib.collection.map]] (I)
  - [[lang.java.lib.collection.map.hash]]
  - [[lang.java.lib.collection.map.weakhash]]
  - [[lang.java.lib.collection.map.identityhash]]
  - [[lang.java.lib.collection.map.sorted]] (I)
    - [[lang.java.lib.collection.map.sorted.navigable]] (I)
        - [[lang.java.lib.collection.map.sorted.navigable.tree]]
  - [[lang.java.lib.collection.map.hashtable]]
    - [[lang.java.lib.collection.map.hashtable.properties]]

## Important Differences

### [[lang.java.lib.collection.s]] vs [[lang.java.lib.collection.interface]]

![[lang.java.lib.collection.interface.list.array#comparison-with-arrays]]

### HashMap vs Hashtable


|               | HashMap                                                        | Hashtable                                                 |
|---------------|----------------------------------------------------------------|-----------------------------------------------------------|
| Introduced in | 1.2                                                            | 1.0                                                       |
| Thread Safety | Not thread safe (not synchronized) => works with single thread | Thread safe (synchronized) => works with multiple threads |
| Speed         | Faster                                                         | Slower                                                    |
| Null key      | One null key allowed                                           | Null key not allowed                                      |

### ArrayList and Vector's only Difference

Vector is thread-safe (most methods are synchronised)
ArrayList is not.

💡 If something is thread-safe, it will inevitably have a lower performance in comparison to a corresponding non-synchronised something.

### `size()` vs `capacity()`

- size = number of objects currently
- capacity = number of objects which can be accommodated
