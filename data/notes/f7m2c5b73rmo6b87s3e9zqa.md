
Java's [[os.memory.ram.user.heap]] implementation.

Used to allocate memory to objects at run time

## How is object stored in memory?

- The actual data/structure that is stored on the heap starts with what's commonly called *object header*.
- Header contains — a (compressed) class pointer
- Class pointer —> an internal data structure
- Internal data structure — defines layout of the class
- Layout of class — stored in a separate memory area called Metaspace (or Compressed Class space if Compressed OOPs are used).
- The pointer can be 4 or 8 bytes, depending on the architecture - even on 64-bit systems, it's usually 4 bytes due to the Compressed OOPs optimization.

## References

- [How references are stored in Java](https://stackoverflow.com/questions/61654407/how-references-are-stored-in-java)
- More about layout of java objects — [Java Objects Inside Out](https://shipilev.net/jvm/objects-inside-out/)
- [Compressed OOPs](https://wiki.openjdk.java.net/display/HotSpot/CompressedOops)
