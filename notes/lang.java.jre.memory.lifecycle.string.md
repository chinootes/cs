---
id: c376iyczea2rtetyc1dgolt
title: String Memory Management
desc: ''
updated: 1713689573361
created: 1712856008805
---

## String Constant Pool

Special memory area in which string literals are stored


## String Initialization using literals

Creating a String literal → [[lang.java.jre.jvm]] checks the String Constant Pool.
  
- Exists => Points to the same 'literal'
- Doesn't Exist => New instance created

## String Initialization using new

```java
String str = new String(); //null
String str = new String("Kya challa?")
```

New object created irrespective of whether the literal already exists or not
