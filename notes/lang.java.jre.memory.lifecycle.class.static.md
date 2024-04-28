---
id: v3bj7bjreqqwo2npxbiz7c6
title: Static members' lifecycle in memory
desc: ''
updated: 1713803859132
created: 1713720230003
---

Static variables are not garbage collected until class is loaded in the memory.

Static variables are referenced by Class objects (❗not class objects) which are referenced by ClassLoaders. So static variables can't be elected for garbage collection while the class is loaded. They can be collected when the respective class loader is itself collected.