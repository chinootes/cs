---
id: 322kyyesffzssad1jqfqxp2
title: Instance Initializer Block
desc: ''
updated: 1712940696274
created: 1712930060562
---

Instance initialisation block can be included in a class. Its simply a block with no name and is called whenever an instance is initialised.

## Order of invokation

Here is the order in which it is invoked with respect to constructors.
**Constructor of parent class → Constructor → Instance initialisation block**

On surface, it looks like the initialisation block is executed first. But what happens is that the compiler copies the block in the constructor at the top. So the constructor is called within which the instance initialiser block runs.

For more details, [[lang.java.paradigms.oo.instantiation.order of invokation]]
