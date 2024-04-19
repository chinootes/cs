---
id: 8hcbbe6jvekm2ossfl77mf7
title: Multiple Inheritance not allowed
desc: ''
updated: 1712931078397
created: 1712930551526
---

- [[paradigm.oo.pillars.inheritance.types.multiple]] is not allowed in some languages
- However, multiple interfaces can be implemented

## Why is Multiple inheritance not allowed?

- To reduce complexity and simplify the language
- **Diamond problem**: Results in ambiguity
    ```mermaid
    classDiagram
        A <|-- B
        A <|-- C
        B <|-- D
        C <|-- D
        class A{ foo() }
        class B{ foo() }
        class C{ foo() }
        class D{ which foo() } 
    ```
- Creates problem during various operations like casting, constructor chaining
- Very few scenarios in which multiple inheritance is required

## Why is multiple inheritance allowed in interfaces?

No ambiguity - implementation is not given by interfaces

## References

[Diamond Problem - StackOverflow](https://stackoverflow.com/questions/2064880/diamond-problem)