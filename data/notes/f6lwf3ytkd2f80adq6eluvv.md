
## How is object stored in memory?

- The actual data/structure that is stored on the heap starts with what's commonly called object header.
- Header contains — a (compressed) class pointer
- Class pointer —> an internal data structure
- Internal data structure — defines layout of the class
- Layout of class — stored in a separate memory area called Metaspace (or Compressed Class space if Compressed OOPs are used).
- The pointer can be 4 or 8 bytes, depending on the architecture - even on 64-bit systems, it's usually 4 bytes due to the Compressed OOPs optimization.

## Reachable Objects

An object is called reachable if it is reachable from a [[lang.java.jre.memory.objects.root]].

Objects which are directly or indirectly reachable from some other objects.

For example,

- P -> O
- P -> Q -> O

O is reachable from P in both cases.

## Root Objects

An object is a root object if it is referenced by:

- A parameter on a call [[stack frame|lang.java.jre.memory#stack-frame]]
- A local variable on the call [[stack frame|lang.java.jre.memory#stack-frame]]
- A [[paradigm.oo.components.modifiers.static.variable]] in class
- Others like [[lang.java.jre.jvm.class loader]] or [[lang.java.lib.jni]] references.

## Lifecycle

```java
Box smallBox;
```

Unlike C++, the above statement won’t create an object. It will just create a reference variable. The reference variable has to be given an object.

```java
Box smallBox= new Box();
```

Now `smallBox` contains address of an object of Box class. That is, it points to the object. However, the object itself has no name.

- Memory is allocated on the [[heap|lang.java.jre.memory#heap-space]] and a reference for that object is returned which is stored in [[stack|lang.java.jre.memory#stack]].