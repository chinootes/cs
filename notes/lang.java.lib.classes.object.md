---
id: 1b17wyzzn4hc4viaeybi3ra
title: Object
desc: 'Object Class'
updated: 1713121959500
created: 1712985840849
---

God class in Java - every class inherits this class implicitly

- Why?
  - By having the Object as the super class of all Java classes, without knowing the type we can pass around objects using the Object declaration.
  - Before generics was introduced, imagine the state of heterogeneous Java collections. A collection class like ArrayList allows to store any type of classes. It was made possible only by Object class hierarchy.
  - The other reason would be to bring a common blueprint for all classes and have some list of functions same among them — methods like [hashCode()](https://javapapers.com/core-java/hashcode-and-equals-methods-override/), clone(), toString() and methods for threading which is defined in Object class.


## Methods

All method are public, final and void unless mentioned otherwise.

| Access and Return Type       | Method      | Parameters              |Function                                                                                 |
|------------------------------|-------------|-------------------------|------------------------------------------------------------------------------------------|
| Object                       | **getClass()**  |                         | returns class object                                                                     |
| int (not final)              | **hashCode()**  |                         | returns hashcode number of the object                                                    |
| boolean (not final)          | **equals()**    | Object                  | compares the provided object with the current object                                     |
| protected Object (not final) | **clone()**     |                         | creates and returns exact copy of object (throws CloneNotSupportedException)             |
| String (not final)           | **toString()**  |                         | returns String representation of the object                                              |
|                              | **notify()**    |                         | wakes up single thread                                                                   |
|                              | **notifyAll()** |                         | wakes up all threads                                                                     |
|                              | **wait()**      | long timeout            | wait for specified milliseconds (throws InterruptedException)                            |
|                              | **wait()**      | long timeout, int nanos | Same as above. Only increases precision.                                                 |
|                              | **wait()**      |                         | Waits until notify() or notifyAll() is invoked by another thread                         |
| protected                    | **finalize()**  |                         | Invoked by garbage collector before object is being garbage collected (throws Throwable) |

### Contract of hashcode() and equals() method

> Equal objects must have equal hashcodes.

💡 If two objects have same hashcode, they may or may not be equal.

Always override hashCode when you override equals. Failure to do so will prevent your class from functioning properly in conjunction with all hash-based collections i.e. HashMap, HashSet etc

It's a common source of bugs.

## References

[hashCode And equals Methods Override - javapapers](https://javapapers.com/core-java/hashcode-and-equals-methods-override/)

