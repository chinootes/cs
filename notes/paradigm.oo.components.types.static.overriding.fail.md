---
id: yn96wb28yho23ro3g3o9wkx
title: Why compiler sometimes talks about overriding static methods?
desc: ''
updated: 1708357537745
created: 1708357503158
---

It means hiding.

From [Overriding v/s Hiding - sanaulla.info](https://sanaulla.info/2008/02/29/overriding-vs-hiding/)
> Sometimes you will see error messages from the compiler that talk about overriding static methods. Apparently, whoever writes these particular messages has not read the Java Language Specification and does not know the difference between overriding and hiding. So they use incorrect and misleading terlminology. Just ignore it. The Java Language Specification is very clear about the difference between overriding and hiding, even if the compiler messages are not. Just pretend that the compiler said "hide" rather than "override".