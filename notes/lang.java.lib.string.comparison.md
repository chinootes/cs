---
id: 9pb2kqfks3q23sdqidit953
title: String Comparison
desc: ''
updated: 1712937954427
created: 1711644046817
---

Strings class implements Comparable [[lang.java.lib.interfaces.marker]].

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
