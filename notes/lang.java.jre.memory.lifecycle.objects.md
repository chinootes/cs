---
id: f6lwf3ytkd2f80adq6eluvv
title: Objects lifecycle in memory
desc: ''
updated: 1713807836105
created: 1713720801067
---

```java
Box smallBox;
```

Unlike C++, the above statement won’t create an object. It will just create a reference variable. The reference variable has to be given an object.

```java
Box smallBox= new Box();
```

Now `smallBox` contains address of an object of Box class. That is, it points to the object. However, the object itself has no name.

- Memory is allocated on the [[lang.java.jre.memory.heap]] and a reference for that object is returned which is stored in [[lang.java.jre.memory.stack]].