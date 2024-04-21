---
id: 6x53s10ue9u0wk8qm3n7ae4
title: Vector
desc: ''
updated: 1713648943085
created: 1713636296847
---

implements [[lang.java.lib.collection.interface.list]] and [[lang.java.lib.interfaces.marker.RandomAccess]]

- Underlying Data Structure: Resizable [[data.structure.primary.array]]
- [[lang.java.lib.collection.tags.duplicates.allowed]]
- [[lang.java.lib.collection.tags.insertion order.preserved]]
- [[lang.java.lib.collection.tags.null insertion.allowed]]
- Best choice for: Frequent retrievel
- Worst choice for: Frequent insertion/deletion in middle
- Constructors:
  1. `Vector v = new Vector();`
  2. `Vector v = new Vector(int initialCapacity);`
  3. `Vector v = new Vector(int initialCapacity, int incrementalCapacity);`
  4. `Vector v = new Vector(Collection C);`
- Default initial capacity: 10
- Load factor/fill ratio:
- New Capacity: 2C

## Vector is legacy class ⇒ Longer method names

- Adding 
    - [[lang.java.lib.collection.interface]] - `add(Object O)`
    - [[lang.java.lib.collection.interface.list]] - `add(int index, Object O)`
    - In vector, `addElement(Object O)`

- Removing
    - [[lang.java.lib.collection.interface]] - `remove(Object O)`
    - [[lang.java.lib.collection.interface.list]] 
        - `remove(int index)`
        - `clear()`
    - In vector,
        - `removeElement(Object O)`
        - `removeElementAt(int index)`
        - `removeAllElements()`


## Child classes/interfaces

[[lang.java.lib.collection.interface.list.vector.stack]]
