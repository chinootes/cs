---
id: algcpxdi0s90k74eafn4rbk
title: Serialization
desc: ''
updated: 1712947843654
created: 1712946929354
---

- 
- An object can be made Serializable by implementing the Serializable [[lang.java.lib.interfaces.marker]].

## SerialVersionUID

- Serialization process associates an ID with each serializable class on runtime → SerialVersionID
- Used to verify that sender and reciever of the serialized object are the same. Throws InvalidClassException otherwise.
- We can generate our own SerialVersionUID by creating a static final long serialVersionUID field in the class. Suggested to have it private and declare it in the class itself.


## `transient` keyword

If you don't want to serialize any data member of the class - that is, you don't want it to be stored - mark it (prefix it) with transient.
