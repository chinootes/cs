
Comparable is used to define natural ordering for user-defined types. 

To do that, the class should implement the `Comparable` interface and define its `compareTo()` method.

## Definition

```java
public interface Comparable<T> {
    int compareTo(T o);
}
```

## Implementation

`compareTo()` has context of two objects. One, which is being used to invoke it and the other, which it takes as an input. It then compares these two objects (the part which is to be implemented) and returns and integer indicating the order.

- **Negative**: current object is less than the other object. 
- **Zero**: current object is equal to the other object. 
- **Positive**: current object is greater than the other object.


```java
compareTo(T o){
 if(this < o) return -1;
 
 if(this == o) return 0;

 if(this > o) return 1;
}
```


## Usage

If a class implements this, you can use the `compareTo()` method to compare its two objects.

```java
switch(obj1.compareTo(obj2)){
    case -1: // obj1 <  obj2
    case 0:  // obj1 == obj2
    case 1:  // obj1 >  obj2
}
```