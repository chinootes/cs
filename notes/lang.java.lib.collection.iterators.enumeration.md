---
id: 4x38t5zqngoe33sug8ec87p
title: Enumeration
desc: ''
updated: 1713681320525
created: 1713680970861
---

- Legacy Interface => Can only be used for legacy classes i.e. [[lang.java.lib.collection.interface.list.vector]] and [[lang.java.lib.collection.map.hashtable]]

## Methods

`public boolean hasMoreElements()`

`public Object nextElement()`

## Usage

```java
//Example
Enumeration e = v.elements(); //v is a vector

while(hasMoreElements()){
Integer I = (Integer) e.nextElements();
}
```

## Limitations

- Applicable only for legacy classes
- Only read operation - can't remove objects
