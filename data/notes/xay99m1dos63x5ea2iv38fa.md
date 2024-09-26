
`andThen` is a method present in functional interfaces such as [[lang.java.lib.interfaces.func.function]], [[lang.java.lib.interfaces.func.function.predicate]] and [[lang.java.lib.interfaces.func.consumer]] to allow you to chain the operations together.

You can pass it a second operation which is supposed to follow the first.

## Definition

```java
R andThen(Function<? super T, ? extends R> after) //R is a functional interface
```

## Usage


```java
Function<String, Integer> stringLength = s -> s.length();
Function<Integer, String> intToString = i -> String.valueOf(i);

Function<String, String> lengthToString = stringLength.andThen(intToString);
String result = lengthToString.apply("Hello"); // "5"
```