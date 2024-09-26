
Casting from subclass to superclass

## Syntax

- Generally, [[type theory.casting.implicit]]. Why?
  
  => Compiler knows that *Cat* is an *Animal.* [[arch.design.oo.principles.solid.liskov]]

## What upcasting gives us?

- [[paradigm.oo.principles.polymorphism]]

    Instead of using different methods for a common functionality in each of the sub classes, we can have a common method in the superclass for that functionality and all subclass objects will be casted implicitly.

    Example - a feed(Animal animal) function to which we can pass objects of Cat and Dog classes → feed(cat); feed(dog);

- [[paradigm.oo.principles.polymorphism.overriding]]

    When an object is upcasted, it still can call overridden methods from its original class.

    For example, if Animal class has an eat() method and subclasses Cat and Dog override it.

    eat(animal) will call the methods from either the class Cat or Dog, whichever it was before upcasting.

    [[paradigm.oo.principles.polymorphism.runtime]] is a result of Upcasting.
