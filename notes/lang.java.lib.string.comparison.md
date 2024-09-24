---
id: lltawdg3ubxo5lujxld7kff
title: String Comparison
desc: ''
updated: 1713644157556
created: 1711644046817
---


Strings class implements [[lang.java.lib.collection.comparable]].

### 1. `equals()` method (**authentication**)

- Two variants
  - public boolean equals (Object another)
  - public boolean equalsIgnoreCase (String another)
- Function
    Compares original content of the String

### 2. `==` operator (**reference matching**)

Compares references not values

### 3. `compareTo()` method (**sorting**)

- Compares _lexicographically_ (dictionary)
- Returns integer value based on the comparison
- s1.compareTo(s2)
  - s1 == s2 ⇒ 0
  - s1 > s2 ⇒ +ve value
  - s1 < s2 ⇒ -ve value
