---
id: anx7b9si477j569e597dkc4
title: Wrapper Classes
desc: ''
updated: 1712937943105
created: 1712856355058
---

- There is a wrapper class for every primitive data type in Java. For example, there’s `Integer` for `int`, `Character` for `char`, `Float` for `float`, `Double` for `double` and so on. That is, the class names are same as the data types’ name (Except char and int) apart from the fact that the class names begin with uppercase letters, which is a convention in Java.
- We can create objects of these wrapper classes instead of variables of primitive data types.
    - `Boolean`
    - `Byte`
    - `Short`
    - `Integer`
    - `Long`
    - `Float`
    - `Double`
- Wrapper classes contains one variable (data member) of their respective primitive data type. They also contain certain functions to manipulate these values.
- Why?
  - Java — primitive data types ⇒ Not objects ⇒ Wrapper classes
  - Also, to make methods available to operate on primitive data types.
- All wrapper classes are [[arch.design.oo.patterns.immutable class]]es
- All wrapper classes implement Comparable [[lang.java.lib.interfaces.marker]]

## Useful Methods

### valueOf()

- Static Method
- Returns object reference of corresponding wrapper class.
- **Syntax**

    ```java
    WrapperClass reference_variable = WrapperClass.valueOf(“Number in string format”, base-decimal by default);
    ```

- **Example**

    ```java
    Integer i1=Integer.valueOf(“123”);
    Integer i2=Integer.valueOf(“101011”,2);
    Double d1=Double.valueOf(“3.14”);
    ```

## parseXxx()

- Static Method
- Xxx can be replaced with any primitive data type
- Similar to valueOf() but returns reference to xxx type rather than a wrapper class object.
- Syntax

    ```java
    xxx**.**varname = WrapperClass**.**parseXxx(“Number in string format”);
    ```

- Example

    ```java
    int a=Integer.parseInt(“123”);
    double b=Double.parseDouble(“13.45”);
    ```

## xxxValue()

- Instance method
- Xxx can be replaced with any primitive data type
- Returns corresponding primitive data type.
- Used to convert from/get the value of a wrapper class object to a primitive data type.
- **Syntax**

    ```java
    xxx varname=objectname.xxxValue();
    ```

- **Example**

    ```java
    //i1 contains a reference of object of Integer class.
    int c = i1.intValue();
    ```


### Methods for [[lang.java.typing.casting.string conversion]]