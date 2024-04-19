---
id: 7o19qqnvgixqmt9g4bp4h6e
title: Dynamic Binding
desc: ''
updated: 1708446217496
created: 1708355056856
---


When the type of object is determined at runtime.

Happens when object of child is assigned to reference of parent.

Example:

```java
Human h = new Student()
//Student IS-A Human
```

```java
foo(Human h) //method definition

//method call
foo(Student s)
```

Reference of Human type ————>       Object of Student type.

(Reference Variable) ---------------->                                           (Object)


# Argument -- `Human h = new Student()` is not dynamic binding

#interview-question

Someone could very easily make an argument that `Human h = new Student()` is not Dynamic Binding

```java
class Human{
    foo(){}
}

class Student extends Human{
    foo(){}
    xyz(){}
}

main(){
    Human h = new Student();
    
    h.xyz(); //This line will give error. 
    h.foo(); 
}
```

## Why it looks like its not runtime polymorphism

The line `h.xyz()` will immediately show an error.

- `h.xyz()`  shows error
- ⇒ Program doesn't know h is an object of class Student
- ⇒ h is an object of Human type
- ⇒ Its not runtime polymorphism

## What actually happens

Compiler doesn't know at compile time that 'h' is an object of Student type.

- Object type determined at runtime
- ⇒ Compiler still thinks 'h' is an object of Human type
- ⇒ COMPILE TIME Error.


Even though we can't call Student-exclusive  methods from this reference without casting, the type of object or the version of method to be called is still determined at runtime. Which still makes it a case of dynamic binding and [[paradigm.oo.pillars.polymorphism.runtime]]. 
