---
id: zzfi2bv83qycdt1insthb3z
title: LinkedList
desc: ''
updated: 1713636260230
created: 1713636201676
---

implements [[lang.java.lib.collection.interface.list]]

- Underlying Data Structure: Doubly Linked List
- Duplicates: Allowed
- Insertion Order: Preserved
- null insertion: Allowed
- Best choice for: Insetion/deletion in middle
- Worst choice for: Random Access
- Constructors:
  1. `LinkedList l = new LinkedList()`
  2. `LinkedList l = new LinkedList(Collection C)`
- Default initial capacity: 0
- Load factor/fill ratio:
- New Capacity:

- References not stored contiguously → no shift operations required while adding/removing elements

- Usually used for implementing Stack and Queue.

    Some specific methods for this purpose:

  - `void addFirst(Object O)`
  - `void addLast(Object O)`
  - `Object getFirst()`
  - `Object getLast()`
  - `Object removeFirst()`
  - `Object removeLast()`
