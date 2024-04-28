---
id: s6akrhxt1lut8w1ua5n50ci
title: Methods' lifecycle in memory
desc: ''
updated: 1713720522675
created: 1713719707742
---

- Private JVM Stack in [[lang.java.jre.memory.stack]] memory is created
- New frame is created and stored in the stack
- [[lang.java.jre.memory.lifecycle.methods.arguments]]
- Frame destroyed when method invocation completes

    A new one will be created again when the method is invoked.