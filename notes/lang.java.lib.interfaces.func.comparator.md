---
id: ip5orztybk9shcn0qhjo7ms
title: Comparator
desc: ''
updated: 1727012158881
created: 1727009611672
---

Allows to define custom ordering of objects. For example, while sorting.

## Definition
```java
@FunctionalInterface
public interface Comparator<T> {
    int compare(T o1, T o2);
}
```

## Usage

```java
class AgeComparator implements Comparator<Person> {
    @Override
    public int compare(Person p1, Person p2) {
        return p1.getAge() - p2.getAge();   

    }
}

public class ComparatorExample {
    public static void main(String[] args) {
        List<Person> people = new ArrayList<>();

        Collections.sort(people, new AgeComparator());
    }
}
```

```java
Collections.sort(people, (p1, p2) -> p1.getAge() - p2.getAge());
```

### Default methods

In addition to the abstract method `compare`, it also provides a bunch of utility methods to easily define a Comparator.

For example,

```java
List<Person> sortedByAge = people.stream()
                                 .sorted(Comparator.comparing(Person::getAge))
                                 .collect(Collectors.toList());

```

Here's a list of all such methods:

- **static comparing([[lang.java.lib.interfaces.func.function]] keyExtractor)**: Like the example above
- **static comparing([[lang.java.lib.interfaces.func.function]], Comparator)**: Like the example above but with Comparator for the given key.

Similar methods but for specific types:

- static comparingDouble
- static comparingInt
- static comparingLong

Lexicographic order sorting (to be used after the above methods):
- thenComparing
- thenComparingDouble
- thenComparingInt
- thenComparingLong

Methods for null friendly Comparator
- nullsFirst(Comparator)
- nullsLast(Comparator)

To modify ordering or comparator: 
- **static naturalOrder**: returns Comparator which compares [[lang.java.lib.collection.comparable]] objects in natural order
- static reverseOrder()
- reversed()


