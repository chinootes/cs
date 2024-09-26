

## Hello World

## Rules

## Naming Conventions

## Comments

## Variables 

### Declaration

### Initialization

### Both at once

## Constants

## Data types

### Primitives

### Compound
 
#### Array

##### Defining

##### Declaring

#### Strings



#### Structures
#### Interfaces

#### Classes

##### Creating objects

##### Using objects



## Operators

### Spread/rest operator

- `...`
    - **Spread**: Used to expand iterables (like array and objects) into individual elements
        - Array Expansion
            ```js
                const arr1 = [1, 2, 3];
                const arr2 = [...arr1, 4, 5];
                console.log(arr2); // Output: [1, 2, 3, 4, 5]
            ```
        - Function Arguments
            ```js
            const numbers = [1, 2, 3];
            const sum = (a, b, c) => a + b + c;
            console.log(sum(...numbers)); // Output: 6
            ```
        - Object Spread
            ```js
                const obj1 = { a: 1, b: 2 };
                const obj2 = { ...obj1, c: 3 };
                console.log(obj2); // Output: { a: 1, b: 2, c: 3 }
            ```
    - **Rest**: Used to collect all arguments into an array.
    ```js
        function sum(...args) {
                return args.reduce((acc, val) => acc + val, 0);
            }   

            console.log(sum(1, 2, 3, 4)); // Output: 10
    ```

    Context within which it is used whether it is a spread or rest operator.

## Flow

### Conditionals

### Loops

## Functions/Methods

### main



