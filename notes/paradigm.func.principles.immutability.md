---
id: gxuhph8erusooz1thpwp9xp
title: Immutability
desc: ''
updated: 1722778311976
created: 1715087569206
---

Functional programming emphasizes immutable data structures, where once a value is assigned, it cannot be changed. Instead of modifying existing data structures, functional programming favors creating new ones. Immutability reduces the risk of unexpected side effects and makes programs easier to reason about.

The functions themselves do not operate on the existing data structures, but you could work around it and mutate the data structure by doing something like:

```python
numbers = filter(lambda x: x % 2 == 0, numbers)
```

This mutates the original data structure. But in the paradigm which is functional programming, this is generally avoided. Instead we create new data structures, promoting clarity, predictability and reasoning about the code.
