---
id: mpyjpsvm6uuozacuhrr78yf
title: Object Type Conversion
desc: ''
updated: 1712884475326
created: 1712883976229
---

- Similarity with primitive conversion

    Converting from one type to another

- Difference

    Primitive type variables store values. So when we convert from a larger to type to smaller type, we might end up loosing information.

    Reference variables on the other hand do not contain the object itself, but its reference. So when we convert types of objects, we're not changing the object, but we're just changing the label on the object, expanding or narrowing the opportunities to work with.

    Upcasting narrows the list of methods and properties available to this object and down casting can extend it.

## [[type theory.casting.object.upcasting]] in Java

[[type theory.casting.implicit]]

## [[type theory.casting.object.downcasting]] in Java

## Syntax

- [[type theory.casting.explicit]]
- Same as narrowing conversion in primitive data types

    ```java
    float a = 10.5;
    int b = (int) a;

    print(a) -→ 10.5
    print(b) -→ 10
    
    Animal animal = new Animal();
    Cat cat = (Animal) animal;    
    ```

- Another way

    ```java
    Animal animal = new Animal();
    if (Cat.class.isInstance(animal)) {
    Cat cat = Cat.class.cast(animal);
    ```

## [[Class Cast Exception]] — ClassCastException

That is why it is advised to use *instanceOf* check before downcasting.

- instanceOf

    Used to avoid the ClassCastException by checking if the object belongs to a certain type

    ```java
    //Example 
    if (animal instanceof Cat) {
        ((Cat) animal).meow();
    }
    
    ```

    ```java
    //case 1
    Dog dog = new Dog();
    Animal animal = dog;

    if(Cat.class.instanceOf(animal)) -→ false

    //case 2
    Cat cat = new Cat();
    Animal animal = cat;

    cat.meow();

    Cat.class.instanceOf(animal) -→ true
    ```

