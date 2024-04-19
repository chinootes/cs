---
id: lafrj3lrli2ks77x9n9ot35
title: Qualified this construct 
desc: ''
updated: 1712955478182
created: 1712955062240
---

[[lang.java.paradigms.oo.inner class.member]] have an implicit reference to an instance of the enclosing (outer) class. **Qualified This** refers to this instance.

If the outer class is A and inner class is B, you can refer to this instance of A from B as `A.this`.

Since we are using a [[lexicography.identifiers.qualifier]] along with `this` [[lang.java.paradigms.oo.objects.context qualifiers]], to form a fully [[lexicography.identifiers.qualified]], it is called "Qualified" `this`.


## Reference

[What does "qualified this" construct mean in java?](https://stackoverflow.com/questions/11276994/what-does-qualified-this-construct-mean-in-java)

> In Effective Java inside the item "Item 22: Favor static member classes over nonstatic" Josh Bloch says:    
>
Each instance of a nonstatic member class is implicitly associated with an enclosing instance of its containing class. Within instance methods of a nonstatic member class, you can invoke methods on the enclosing instance or obtain a reference to the enclosing instance using the qualified this construct.