---
id: nwt68evbhbbvfha3pwsgm29
title: Initialization of iterators
desc: ''
updated: 1713681767660
created: 1713681460454
---

[[lang.java.lib.collection.iterators.enumeration]], [[lang.java.lib.collection.iterators.iterator]], [[lang.java.lib.collection.iterators.iterator.list]] are all interfaces


How can we create objects for interfaces then?
⇒ **We don't**.

What happens actually, is that the elements() method has a class within it which implements Enumeration interface. elements() returns the object of that class. This is how it works for other two cursor interfaces as well.

```java
System.out.println(c.getClass().getName()); //c is an object of a iterator
```
Output - 
```java
vector$1              // if c is an Enumeration Object
vector$Itr            // if c is an Iterator Object
vector$ListItr        // if c is a List Iterator Object
```

`vector$` means inner class of vector ( or whichever Collection class we're getting the object for)

1 means it is an anonymous inner class

`Itr` and `ListItr` are names of [[lang.java.paradigms.oo.inner class]]es implementing Iterator and ListIterator respectively.
