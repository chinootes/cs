---
id: eo18wj1qkvnrnnyp86ggakx
title: ArrayList
desc: ''
updated: 1713677679463
created: 1713635957884
---

implements [[lang.java.lib.collection.interface.list]] and [[lang.java.lib.interfaces.marker.RandomAccess]]

- Underlying Data Structure: Resizable Array
- [[lang.java.lib.collection.tags.duplicates.allowed]]
- [[lang.java.lib.collection.tags.insertion order.preserved]]
- [[lang.java.lib.collection.tags.null insertion.allowed]]
- Best choice for: Frequent Retrieval (Random Access)
- Worst choice for: Frequent Insertion/deletion in middle -> Several shift operations are required
- Constructors:
   1. `ArrayList l = new ArrayList();`
   2. `ArrayList l = new ArrayList(int initialCapacity);`
   3. `ArrayList l = new ArrayList(Collection C);`
- Default initial capacity: 10
- Load factor/fill ratio:
- New Capacity: 1.5C + 1

References are stored contiguously (not the objects).

## Comparison with Arrays



|                        | [[data.structure.primary.array]]                                                                                                                                                              | ArrayList                                                                                                  |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Definition             | An array is a dynamically-created object. It serves as a container that holds the constant number of values of the same type. It has a contiguous memory location. | The ArrayList is a class of Java Collections framework.                                                    |
| Size                   | Static - fixed-length data structure                                                                                                                               | Dynamic - variable length data structure - can resize itself when needed                                   |
| Size specification     | Mandatory to provide size while initializing                                                                                                                       | Size can be left unspecified - default initial capacity will be used                                       |
| Performance            | Fixed size => Faster                                                                                                                                               | Internally backed by array. Resize operation slows down the performance                                    |
| Primitive/generic type | Can store both primitives and objects                                                                                                                              | Can't store primitives - automatically converts them to objects. For example, int is converted to Integer. |
| Getting the length     | arr.length                                                                                                                                                         | arr.size()                                                                                                 |
| Adding elements        | Can add elements using assignment operator                                                                                                                         | add() function                                                                                             |
| Multiple dimensions    | Can be multi-dimensional                                                                                                                                           | CAN'T be multi-dimensional                                                                                 |
