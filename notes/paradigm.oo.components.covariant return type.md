---
id: 86y76iubiyrpvkrgh5neg49
title: Covariant Return Type
desc: ''
updated: 1708239448883
created: 1708239382370
---

When [[type theory.variance]] of return types if covariant.


Two examples where this can work -

- Suppose there are two classes A and B. A has a function with return type A and B has the function with the same name and arguments but with return type B. The function in B can override the one in A in this situation.
- Suppose there are four classes A, B, C and D. A is inherited by C and B is inherited by D. Now C has a function with return type A and D has a method with same name and arguments with return type B. Method overriding works here.

Basically, the parent return type is being replaced by child return type in the overriding method.
