
If a language supports [[dev.issues.exception.declaration]], this is how it likely works with method overriding.

## Case 1: Super class doesn't declare an exception

Sub class overridden method:

- cannot declare a [[dev.issues.exception.types.checked]] but
- can declare an [[dev.issues.exception.types.unchecked]].

## Case 2: Super class declares an exception

Sub class overridden method

- can declare
  - same exception
  - subclass exception ([[type theory.variance]] = covariant)
  - or no exception
  but
- cannot declare parent exception
