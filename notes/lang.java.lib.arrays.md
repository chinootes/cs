---
id: c4uuhel2q5rxra533rveq1z
title: Arrays
desc: ''
updated: 1712949673989
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
    System.out.println(x.getClass().getName());
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

- Every array type implements Serializable  and Cloneable [[lang.java.lib.interfaces.marker]]s. 
- Arrays can be assigned to variables of type Object — [[type theory.casting.object.upcasting]].
- All methods of Object class can be invoked on an array

## References

- [Is an array a primitive type or an object in Java? - GeeksforGeeks](https://www.geeksforgeeks.org/array-primitive-type-object-java/)
- [Chapter 10. Arrays - Oracle Docs](https://docs.oracle.com/javase/specs/jls/se7/html/jls-10.html)
