---
id: wl01yrgrwn2hs63gp5mahq9
title: Exceptions
desc: ''
updated: 1713121019042
created: 1713117416265
---

## [[programming.exception.types.checked]]

Classes which directly inherit Throwable except RuntimeExceptions and Errors.

## [[programming.exception.types.unchecked]]

Classes which inherit RuntimeExceptions


## Handling

### Catching

- `try`
    - Used to specify a block of code which can throw an exception.
    - Must be followed by a catch or finally.
    - Can't be used alone

- `catch`
    - Block used to handle the error.
    - Must be preceded by try
    - Can't be used alone

### Always execute

- `finally`

Contains the code which must be executed irrespective of whether an exception is handled or not

### Throwing

- `throw`

Used to throw an exception

- `throws`
    - Used to declare exceptions
    - Doesn't throw error
    - Specifies that an exception may occur in a method
    - Used with method signature

## Creating Custom Exceptions

- How to create?

    Create a class WhateverException which extends Exception

- How to return your custom message while throwing exception?

    Pass the message you want to show as a String to the Exception (or super).

- Are custom exceptions checked or unchecked?

    If you want it to be checked, extend Exception. If you want it to be unchecked, extend RuntimeException.

## Propagation

### Exceptions in main() method

- What happens when main() throws an error?

    Java Runtime terminates the program and print the exception message and stack trace in system console.

- Can *throws* keyword be used with main()?

    Yes, it can be used. Although, there's no reason for a `main` method to `throw` anything. Since, any error will handled by JVM in the same way.

## Exceptions raised in common scenarios


Scenario | Exception | 
----------------|-----------|
 Divide by zero | `ArithmeticException` |
 Operation on Null Pointer   | `NullPointerException` |
 Operating on incorrect/non-existant index    | `ArrayIndexOutOfBoundsException` | 
| Wrong formatting of any value. For example, converting a String variable with characters into digit. |`NumberFormatException`|
