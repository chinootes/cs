---
id: tv91pcfe2tgsqlzk67vgbrp
title: Object Oriented Design and Programming
desc: ''
updated: 1708452976545
created: 1708179490422
---

## Entities/Components

- [[paradigm.oo.components.class]]
- [[paradigm.oo.components.object]]
- [[paradigm.oo.components.class.friend]]
- [[paradigm.oo.components.members]]
- [[paradigm.oo.components.covariant return type]]

## Four Pillars + one secret basement of OOP

- [[paradigm.oo.pillars.polymorphism]]
  - [[paradigm.oo.pillars.polymorphism.overloading]]
  - [[paradigm.oo.pillars.polymorphism.overriding]]: [[paradigm.oo.components.covariant return type]]
- [[paradigm.oo.pillars.inheritance]]
  - [[paradigm.oo.pillars.inheritance.types.single]]
  - [[paradigm.oo.pillars.inheritance.types.multilevel]]
  - [[paradigm.oo.pillars.inheritance.types.multiple]]
  - [[paradigm.oo.pillars.inheritance.types.hierarchical]]
  - [[paradigm.oo.pillars.inheritance.types.hybrid]]
- [[paradigm.oo.pillars.encapsulation]]
- [[paradigm.oo.pillars.abstraction]] \ [[paradigm.oo.components.types.abstract]]
  - [[paradigm.oo.components.interface]] \ [[paradigm.oo.components.types.abstract.class]] 
  - [[arch.design.oo.use cases for.abstract class]]
    - [[arch.design.oo.use cases for.abstract class.providing flexible behavior for related classes]]
    - [[arch.design.oo.use cases for.abstract class.helper]]
    - [[arch.design.oo.use cases for.abstract class.stepping stone]]
- [[paradigm.oo.pillars.association]]
  - [[paradigm.oo.pillars.association.aggregation]]
    - [[paradigm.oo.pillars.association.aggregation.composition]]
      - [[arch.design.oo.principles.composition over inheritance]]
        - [[paradigm.oo.pillars.inheritance.purpose]] vs [[paradigm.oo.pillars.inheritance.disadvantages]]
        - [[paradigm.oo.pillars.association.aggregation.composition.benefits]] vs [[paradigm.oo.pillars.association.aggregation.composition.disadvantages]]

## OOP Features

- [[paradigm.oo.features.binding.static]]
- [[paradigm.oo.features.binding.dynamic]]
- [[paradigm.oo.pillars.polymorphism.runtime]]
- [[paradigm.oo.features.shadowing]]
- [[type theory.substitutability]]
- [[type theory.variance]]

## Types of members/classes

- [[paradigm.oo.components.types.static]]
  - [[paradigm.oo.components.types.static.variable]]
: [[paradigm.oo.components.types.static.variable.serialization]]
  - [[paradigm.oo.components.types.static.method]]: [[paradigm.oo.components.types.static.method.accessing instance variables]]
  - [[paradigm.oo.components.types.static.access using objects]]
  - [[paradigm.oo.components.types.static.overriding]]
  - [[paradigm.oo.components.types.static.overriding.fail]]
- [[paradigm.oo.components.types.final]]
- [[paradigm.oo.components.types.abstract]]: [[paradigm.oo.components.types.abstract.class]]

## Accessing/referring objects

- [[paradigm.oo.context.object.self-reference]]
- [[paradigm.oo.context.object.super]]

## Playing with Objects

- [[paradigm.oo.components.object.cloning]]
- [[type theory.casting.object]]: [[type theory.casting.object.upcasting]] \ [[type theory.casting.object.downcasting]]
- [[paradigm.oo.components.object.serialization]]
- [[paradigm.oo.components.object.deserialization]]

## Object Oriented Design

- [[arch.design.oo.application with no constraints]]
- [[arch.design.oo.use cases for.interface]]
- [[arch.design.oo.use cases for.abstract class]]
  - [[arch.design.oo.use cases for.abstract class.providing flexible behavior for related classes]]
  - [[arch.design.oo.use cases for.abstract class.helper]]
  - But it is okay to use [[arch.design.oo.use cases for.abstract class.stepping stone]]

### [[arch.design.oo.patterns]]

- [[arch.design.oo.patterns.gof]]
  - [[arch.design.oo.patterns.gof.creational]]s
    - [[arch.design.oo.patterns.gof.creational.singleton]]
    - [[arch.design.oo.patterns.gof.creational.factory]]
    - [[arch.design.oo.patterns.gof.creational.builder]]
    - [[arch.design.oo.patterns.gof.creational.dependency injection]] and [[arch.design.oo.principles.ioc]]
      - [[Dependency]]
      - [[arch.design.oo.patterns.gof.creational.dependency injection.constructor]]
      - [[arch.design.oo.patterns.gof.creational.dependency injection.setter]]
      - [[arch.design.oo.patterns.gof.creational.dependency injection.parameter]]
      - [[arch.design.oo.patterns.gof.creational.dependency injection.backdoor]]
  - [[arch.design.oo.patterns.gof.structural]]
    -[[arch.design.oo.patterns.gof.structural.marker]]
  - [[arch.design.oo.patterns.gof.behavioural]]
    - [[arch.design.oo.patterns.gof.behavioural.dao]]
    - [[arch.design.oo.patterns.gof.behavioural.strategy]]
    - 