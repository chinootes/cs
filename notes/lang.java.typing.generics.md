---
id: hvxpw3bn5gil1aogfdkx8y8
title: Generics
desc: ''
updated: 1726998525217
created: 1726996952912
---

- Generics are **parameterized types** in Java.
- This allows types like Integer, String or user-defined types to be a parameter to methods, classes or interfaces.

## Types

- Generic classes
- Generic methods
- Generic interfaces

## Defining 

### Naming convention

- T – Type
- E – Element
- K – Key
- N – Number
- V – Value

### Classes

```java
class Test<T> {
    T obj;
    Test(T obj) { this.obj = obj; } 
    public T useT() { return this.obj; }
}
```

Multiple types
```java
class Test<T, U>{
    T obj1;  
    U obj2;   

    Test(T obj1, U obj2){
        this.obj1 = obj1;
        this.obj2 = obj2;
    }
}
```

### Methods
```java
class Test {
    static <T> void genericMethod(T element)
    {
//        element...
    }
 
```

## Usage

- Generics work only with reference types
    ```java
    Test<int> obj = new Test<int>(20); //compile time error
    ```
- They work with primitive arrays since those are also references.
    ```java
    ArrayList<int[]> a = new ArrayList<>();
    ```
- Generic types maintain type safety. Different types behave differently. For example, you can't assign a generic initialized with `Integer` to a generic initialized with `String`.


## References

- [Generics in Java - GFG](https://www.geeksforgeeks.org/generics-in-java/)