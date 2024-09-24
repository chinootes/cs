---
id: c5elrg6xfbs9jqfrh4kqo2e
title: Immutable Class
desc: ''
updated: 1727116810248
created: 1712859683855
---

Cannot be changed (mutated)

Whenever changed - a new instance is created


## What makes a class immutable?

- Instance variable is final (value can't be changed)
- class = final - So subclass can't be created
- No setters

## How to create an immutable class

- Create **final** class with all **final data members**.
- Whichever way you decide to initialize the object and add value to these fields make sure to perform a [[deep cloning|paradigm.oo.components.object.cloning#deep-cloning]] for any reference fields.
- You have to be careful when there's a reference in the members as well. For example, arrays in Java are mutable objects. 

💡 Use [[clone method|lang.java.paradigms.oo.objects.cloning]] to perform deep cloning. You can use the same method for any [[lang.java.lib.interfaces.marker.cloneable]] object.

```java
final public class ImmutableClass {
  final private int id;
  final private Map<String, Integer> m;
  final private int[] arr;

  public ImmutableClass(int id, HashMap<String, Integer> m, int[] a){
      this.id = id;
      this.m = new HashMap<>();
      this.arr = arr.clone();
      

      for (String key : m.keySet()) {
          this.m.put(key, m.get(key));
      }
  }

    public int getId() {
        return id;
    }

    public int getMapValue(String key){
      return this.m.getOrDefault(key, -1);
    }

    public int[] getArr(){
        return arr.clone()
    }
}
```

## Benefits 

The main benefits of immutability come in case of multi-threaded applications, functional programming and high-security systems.

- Thead safety
- Predictable behavior
- Enhanced security: ensures that sensitive data cannot be modified after its created preventing unintended or malicious change.
- Caching: 
    - Immutable objects can be safely shared across different parts of program.
    - Hashcodes for hash-based structures can be precomputed and cached - since they won't change
- Works well with [[paradigm.func]]
    - Immutability is one of the principles of functional programming
    - Immutable objects ensure that functions don't modify anything outside their scope

## Use cases

- 

## References

- [How To Create an Immutable Class in Java](https://arc.net/l/quote/zfjjlivr)
- [Java Immutable Class - Builder Pattern](https://www.journaldev.com/1432/java-immutable-class-builder) _dead_
    - [Archive Link](https://web.archive.org/web/20220704144259/https://www.journaldev.com/1432/java-immutable-class-builder)
- [Why do we need immutable class?](https://stackoverflow.com/questions/3769607/why-do-we-need-immutable-class)