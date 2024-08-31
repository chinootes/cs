---
id: l6kravc26pl7ixjyg5o3nlk
title: Arrays
desc: ''
updated: 1724572241535
created: 1712949538100
---



## Arrays in Java are Objects

- This is why arrays are initialized using `new` keyword
- For each array type, there exists a corresponding class.
  - So there is a class for int[], for float[], double[] etc.
  - These classes are the part of java language and not available to the programmer level
  - To know the class of any array

    ```java
    // Here x is the name of the array.
    Sys
    ```

### Corresponding class names for some array types
```plain text
Array typeCorresponding          Class Name
int[]                            [I
int[][]                          [[I
double[]                         [D
double[][]                       [[D
short[]                          [S
byte[]                           [B
boolean[]                        [Z
```

>[ for single dimension
[[ for two-dimensional

- Every array type implements [[lang.java.lib.interfaces.marker.serializable]]  and [[lang.java.lib.interfaces.marker.cloneable]]. 
- Arrays can be assigned to variables of type Object — [[type theory.casting.object.upcasting]].
- All methods of Object class can be invoked on an array

## `Arrays` Methods 

- `Arrays.sort(arr)`
- `Arrays.fill(arr,0)`: Fills all elements of an array with the passed value.

## References

- [Is an array a primitive type or an object in Java? - GeeksforGeeks](https://www.geeksforgeeks.org/array-primitive-type-object-java/)
- [Chapter 10. Arrays - Oracle Docs](https://docs.oracle.com/javase/specs/jls/se7/html/jls-10.html)
