
In Java [[paradigm.func.components.lambda]]s are defined as below:

```java
(parameters) -> expression;
```

Brackets for parameters are optional if there is only one parameter and its type is inferred.


```java
List<String> list = Arrays.asList("a", "b", "c");
list.forEach(item -> System.out.println(item));
```
