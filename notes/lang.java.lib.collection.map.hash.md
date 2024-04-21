---
id: wkd10knym4zof3fc6jvgd0q
title: HashMap
desc: ''
updated: 1713648663312
created: 1713642025198
---


implements [[lang.java.lib.collection.map]]

[[lang.java.lib.collection.tags.thread safety.not safe]]

## Initialization

```java
Map map = new HashMap();
```

or

```java
Map<String, String> map = new HashMap<String, String>();
```

## Methods

- `map.put("key", "value");`
- `map.get("key");` → value
- `keySet()` → Set of keys

What happens when Repeating/duplicate keys ⇒ value gets replaced

- Fixed Order insertion → Linked HashMap
- Sorting Order → Tree HashMap

## Implementation


```java
HashMap <K,V> implements Map<K,V>
{
Entry <K,V> {} //Inner class
Entry next; //reference to another entry to store entries like linked lists

int hash; //Hashvalue of key to avoid calculating everytime its  needed
}
```

- Initial Capacity

    16 (Array of 0-15)

- Load factor - After the load factor (percentage) is reached, the capacity automatically increases

    0.75

  - So when the array is filled more than 75%, the table size doubles to 32.
  - The hashtable is rehashed (Internal data structures are rebuit)
- Java 8 improvement

    When the number of nodes in a HashMap reaches the TREEIFY_THRESHOLD, the nodes are converted to TreeNode. Basically, from linked list to a balanced tree. This improves the worst case performance from O(n) to O(log n). After the HashMap becomes small due to removal or resizing, TreeNodes are converted back to nodes.

- HashMap Bucket Resizing Overhead

    You should create HashMap with initial capacity close to your expected volume. If its too small, and the load is in millions, whenever the bucket will reach its load factor it will resize and rehash → which is a very costly operation. Also, make sure to use full capacity else a lot of memory of unused blocks will go wasted.
    
## References

- [How HashMap works in Java? With Animation!! whats new in java8 tutorial](https://www.youtube.com/watch?v=c3RVW3KGIIE)
- [Java 8 HashMap Implementation and Performance - DZone Java](https://dzone.com/articles/java8-hashmap-implementation-and-performance)
