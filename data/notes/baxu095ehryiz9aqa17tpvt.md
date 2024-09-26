
Framework for processing sequences of data in declarative and functional style.

Basically, you can specify an operation and perform it for all items in the collection.


## Intermediate Operations

Intermediate operations return a stream.

### `filter`([[lang.java.lib.interfaces.func.function.predicate]])

Filters elements based on a condition.

 ```java
 List<Integer> evens = numbers.stream()
                             .filter(n -> n % 2 == 0)
                             .collect(Collectors.toList());
  ```

### `map`([[lang.java.lib.interfaces.func.function]])

Transform each element of the stream.

```java
List<String> upperNames = names.stream()
                               .map(String::toUpperCase)
                               .collect(Collectors.toList());
```

### `flatMap`([[lang.java.lib.interfaces.func.function]])
 
Flattens stream of streams into a single stream.

```java
List<String> allWords = sentences.stream()
                                 .flatMap(sentence -> Arrays.stream(sentence.split(" ")))
                                 .collect(Collectors.toList());

```
```java
Stream<List<Integer>> nestedStream = Stream.of(List.of(1, 2), List.of(3, 4));
Stream<Integer> flattenedStream = nestedStream.flatMap(List::stream);
```


### `distinct()`

Removes duplicates.
```java
List<Integer> uniqueNumbers = numbers.stream()
                                     .distinct()
                                     .collect(Collectors.toList());

```

### `sorted()` and `sorted`([[lang.java.lib.interfaces.func.comparator]])

Sorts by natural order or by Comparator, if passed.
```java
List<String> sortedNames = names.stream()
                                .sorted()
                                .collect(Collectors.toList());
```

```java
List<Person> sortedByAge = people.stream()
                                 .sorted(Comparator.comparing(Person::getAge))
                                 .collect(Collectors.toList());
```

### `peek`([[lang.java.lib.interfaces.func.consumer]])

Performs an action on each element without altering the stream.

```java
numbers.stream()
       .peek(n -> System.out.println("Processing number: " + n))
       .collect(Collectors.toList());
```

### `limit(long n)`

Limits the stream to first n elements.

```java
List<Integer> firstThree = numbers.stream()
                                  .limit(3)
                                  .collect(Collectors.toList());
```

### `skip(long n)`

Skips the first n elements.

```java
List<Integer> withoutFirstTwo = numbers.stream()
                                       .skip(2)
                                       .collect(Collectors.toList());

```


### Terminal Operations

These operations consume the stream and return a result.

### `forEach`([[lang.java.lib.interfaces.func.consumer]])

Performs an operation for each element.
```java
names.stream().forEach(System.out::println);
```

### `collect(Collector)`

Collects the stream into a collection.
Instance of Collector can be fetched from [[lang.java.lib.classes.collectors]] API.


```java
List<String> collectedNames = names.stream().collect(Collectors.toList());
```

### `<U> U reduce(U identity,` [[lang.java.lib.interfaces.func.function.BinaryOperator]]` accumulator)`

Reduces stream to a single value.

- `identity` value is used as the initial value
- `accumulator` function is used to combine all the elements.

```java
int sum = numbers.stream()
                 .reduce(0, Integer::sum);

```

### `toArray()`
Converts stream into array.
```java
String[] nameArray = names.stream().toArray(String[]::new);
```

### `min`([[lang.java.lib.interfaces.func.comparator]]) and  `max`([[lang.java.lib.interfaces.func.comparator]])

```java
Optional<Integer> min = numbers.stream()
                               .min(Comparator.naturalOrder());

```

### `count()` 
```java
long count = numbers.stream().count();
```
### `anyMatch`([[lang.java.lib.interfaces.func.function.predicate]]), `allMatch`([[lang.java.lib.interfaces.func.function.predicate]]) and `noneMatch`([[lang.java.lib.interfaces.func.function.predicate]])

```java
boolean hasEven = numbers.stream()
                         .anyMatch(n -> n % 2 == 0);
```

### `findFirst()`
```java
Optional<Integer> first = numbers.stream()
                                 .findFirst();

```
### `findAny()` 

```java
Optional<Integer> any = numbers.stream()
                               .findAny();

```

---
Introduced in [[lang.java.v.8]]