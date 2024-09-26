
Collection framework provides iterator interfaces like `Enumeration`, `Iterator` and `ListIterator` to iterate over the elements within a collection. 

`Enumeration` is a legacy interface. While `ListIterator` is a child of `Iterator` specifically for lists.

## Use cases and Trade Offs

- `Enumeration` can only be used for [[legacy collections|lang.java.lib.collection#legacy-collections]] like `Vector` and `Hashtable`. Also, it supports only **read operations**.
- `Iterator` is the most commonly used since it can be used for any Collection. It can be used to remove but not for replacing or adding new object.
- Both `Enumeration` and `Iterator` are only forward direction cursor
- `ListIterator` is the most powerful cursor which is bidirectional and has methods to remove, replace and add new objects. But it can only be used for `List` collections.


## Initialization

```java
 Enumeration e = v.elements(); //v is a vector
 Iterator itr = c.iterator(); //c is any collection object
 ListIterator litr = l.listIterator(); //l is any List object
``` 

But all the iterators mentioned above are interfaces.

How can we create objects for interfaces then? ⇒ **We don't**.

These methods being used to initialize the iterators have a class within them which implements the corresponding interface. The object of this class is then returned. 

```java
System.out.println(i.getClass().getName()); //i is an object of a iterator
```

Output:
```java
vector$1              // if c is an Enumeration Object
vector$Itr            // if c is an Iterator Object
vector$ListItr        // if c is a List Iterator Object
```

`vector$` means inner class of vector ( or whichever Collection class we're getting the object for)

1 means it is an anonymous inner class

`Itr` and `ListItr` are names of [[lang.java.paradigms.oo.inner class]]es implementing Iterator and ListIterator respectively.



## Methods

### Enumeration
- `public boolean hasMoreElements()`
- `public Object nextElement()`


### Iterator

- `public boolean hasNext()`
- `public Object next()`
- `public void remove()`

### List Iterator

Forward

- `public boolean hasNext()`
- `public Object next()`
- `public int nextIndex()`

Extra capabilities

- `public void remove()`
- `public void set(Object new)` → replace
- `public void add(Object new)`

Backward

- `public boolean hasPrevious()`
- `public Object previous()`
- `public int previousIndex()`

The `set()` method of `ListIterator` interface is used to replace the last element which is returned by the `next()` or `previous()` along with the given element. The call can be added only if neither `remove()` nor `add(E)` method have been called.
