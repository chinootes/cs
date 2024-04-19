---
id: 2417fhwdcstfomven5lddt9
title: Variance
desc: ''
updated: 1708358297412
created: 1708237966152
---

Variance defines how the type relations of complex types will vary or hold in their components( entities and components in programming languages like enumerables (enums), functions, arrays, lists etc).

We know how [[type theory.substitutability]] works in case of objects. This kind of replacement can also be done with the components of these types. This is called variance.

- When objects are replaced — substitutability
- When components are replaced — variance

For example, a type Cat and Animal, where Animal is parent (or whatever) of Cat. Variance defines how the subtypes of Cat and subtypes of Animal will either hold or deviate from this relation.

The relation is:

- **variant** if the relation is somehow carried on to the components or children, either holding the relation or reversing the relation.
    - **covariant** if it preserves the ordering of types.
    - **contravariant** if it reverses this order. 
    - **bivariant** if both of the above apply
- **invariant** or **nonvariant** if the relation is not carried on to the components or children.

## Thoughts on deciding variance

While designing any type system, variance is considered by the designer. 
- Contravariance is usually considered unintuitive by programmers. This can lead to complex typing rules.
- If the type system is variant, the type system is considered to be well-typed.
- Sometimes the designer will choose to keep it invariant to keep the type system simple. But this could voilate type-safety.
 