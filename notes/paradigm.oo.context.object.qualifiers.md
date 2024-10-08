---
id: gos7shmfukhobg64yy9murs
title: Object Context Qualifiers
desc: ''
updated: 1715083639209
created: 1712953689422
---

# A note on Object Context Qualifiers

You'll find this term being used at some places in these notes. The term "Object Context Qualifiers" is not used anywhere generally and is not a "real" Computer Science term, AFAIK. Its a term I use for my understanding to refer to keywords which are used to discern or "qualify" the context of a member in an object, that is, to identify if a member being referred to is a member of the current class of the object, or its superclass.

## Reasons why it makes sense

1. [[dev.lingo.identifiers.qualifier]]s do refer to lexical tokens which are used to remove ambiguity while identifying entities. So that's where this comes from.
2. Another reason is Java's [[lang.java.paradigms.oo.inner class.member.qualified this]].
3. These keywords are used in object contexts, not static ones.