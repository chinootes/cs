---
id: 8pr6ulaidsozf1jx51go0f9
title: Exceptions
desc: ''
updated: 1713120934478
created: 1713120316941
---

## [[programming.exception.types.checked]]


## [[programming.exception.types.unchecked]]


## Handling

### Catching

- ``
    - Used to specify a block of code which can throw an exception.
    - Must be followed by a ``.
    - Can't be used alone

- ``
    - Block used to handle the error.
    - Must be preceded by ``
    - Can't be used alone

### Always execute

- ``

Contains the code which must be executed irrespective of whether an exception is handled or not

### Throwing

- ``

Used to throw an exception

### Declaring 

- ``
    - Used to declare exceptions
    - Doesn't throw error
    - Specifies that an exception may occur in a method
    - Used with method signature

### Creating Custom Exceptions

- How to create?

- How to return your custom message while throwing exception?

- Are custom exceptions checked or unchecked?

## Propagation

## Exceptions in main() method

- What happens when main() throws an error?


- Can *throws* keyword be used with main()?



## Exceptions raised in common scenarios


Scenario | Exception | 
----------------|-----------|
 Divide by zero | `` |
 Operation on Null Pointer   | `` |
 Operating on incorrect/non-existant index    | `` | 

