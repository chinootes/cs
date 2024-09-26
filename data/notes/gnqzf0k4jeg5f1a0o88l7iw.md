

## Hello World

```java
public class HelloWorld{
 public static void main(String[] args){
  System.out.println("Hello World");
 }
}
```

## Rules

1. Outer Class - Always public or default
2. There can be only one public class in a java file.
3. File name = (public,if any) class name
4. Every function has to be a member function of a class. Even main function.
5. Main function’s prototype is fixed `public static void main(String[] args)`
6. No semicolon after class definition.
7. Semicolon after every statement.

## Naming Conventions


- PascalCase for class names.
- camelCase for methods, objects and variable names.
- UPPERCASE for constants

## Comments

```java
/*Multiple Line*/
//Single Line
/** Documentation Style*/
```


## Variables 

### Declaration

### Initialization

### Both at once

## Constants

Prefixing `final` keyword to the  declaration+ initialization.

### Blank final variable

Final variable not initialised during declaration

All final variables must be initialised, or else => Compile time error

=> These have to be initialized later, in constructor or somewhere.

> It might not sound correct to call it variable since by definition, `final` means constant, so by behaviour, it doesn't vary.
> But these variables can vary once.

#### Ways to initialise
  
- Can be initialised within an [[lang.java.paradigms.oo.instantiation.iib]]
- Can be initialised within a constructor
- If there are multiple constructors
- Initialise in all of them, or else => Compile time error


#### Blank static final member/_variable_

Blank final _variable_ which is [[paradigm.oo.components.modifiers.static]].

##### Initialisation

Only within static block.


## Data types

### Primitives

- `byte`
  - 8 bits and signed
- `short`
  - 16 bits and signed
- `char`
  - 16 bits and unsigned, so that it may represent Unicode characters
- `int`
  - 32 bits and signed
- `long`
  - 64 bits and signed
- `float`
  - 32 bits and signed
- `double`
  - 64 bits and signed
- `boolean`
  - it's not numeric, may only have true or false values

#### Suffixing for Non-default Primitive Data Types

- `int` and `long`

    Default type for integer literals is `int`. That is, unless specified otherwise, 35 is an `int`. So if we assign an integer directly to a `long` variable, it will result in compilation error.

    ```java
    //Compilation error
    long x = 232342;
    ```

    Thus, we have to specify explicitly that the value 232342 is a `long`.

    This can be done by suffixing `l` or `L` to the value. For example. `232342L`.

- `float` and `double`

    Similarly, double is the default value for floating point literals. Unless explicitly stated, 9.5 is a `double` not a `float`.

    ```java
    float a = 3.7 // 3.7 is a double, ‘a’ is float => Error
    float a = 3.7f // a is a float
    ```

#### Prefixing for Different Bases

- **Decimal**: `127`
- **Hexadecimal**: `0x7f` (Prefix - `0x`)
- **Octal**: `0177` (Prefix - `0`)
- **Binary**: `0b10011001` (Prefix - `0b`)

### Compound
 
#### Array

##### Declaration
```java
int[] arr;
```

```java
int a[];
```

Array can be defined in java in the above two ways. However, unlike C++ defining an array actually means that we are defining a pointer, which will point to an array.

##### Initialization

```java
int arr[] = new int(3)
```

#### Strings

##### Declaration

```java
String s;
```

##### Initialization

```java
s = new String();
```

```java
s = new String("string");
```
```java
s = "string";
```

##### Both at once

```java
String s = new String();
```
```java
String s = new String("string");
```
```java
String s = "string";
```

##### Length 

```java
s.length();
```

##### Looping/character at index

```java
s.charAt(i);
```
#### Structures
#### Interfaces

#### Classes

##### Creating objects

```java
Box smallBox;
```

Unlike C++, the above statement won’t create an object. It will just create a reference variable. The reference variable has to be given an object.

```java
Box smallBox= new Box();
```

Now `smallBox` contains address of an object of Box class. That is, it points to the object. However, the object itself has no name.

##### Using objects

Through its reference.

```java
class Example 
 {
 public static void main(String[] args)
  {
   Box smallBox=new Box();
   smallBox.setDimension(12,10,5);  
   smallBox.showDimension; 
  /*From the perspective of C++, 
  it looks like smallBox is the name of an object. 
  Though its not.*/
   
   smallBox= new Box();
  /*smallBox will now refer to a new object 
  and the older object will become ‘Garbage Block’, 
  which will get destroyed 
  when Garbage collector will run.*/

  smallBox.showDimension();
  /*Will print 0,0,0 since no value is assigned. 
  The default value is 0.*/
  }
}
```

## Operators

## Flow

### Conditionals

### Loops

## Functions/Methods

### `public static void main(String[] args)`

- **`public`**: So that JVM can call main function from outside of the class body.

- **`static`**: Static member functions can be called without an object.

- **`void`**: Always — no return type

- **Argument**: `String[] args`. Array of strings




