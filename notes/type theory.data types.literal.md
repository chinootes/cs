---
id: 50g8rcmy0ufbguex5drq98m
title: Literal Type
desc: ''
updated: 1713902749070
created: 1713901444103
---

A literal type is a value, enforced as a type.

That means, a variable of literal type can only have value of the [[dev.lingo.literal]] and nothing else.

You can say it is a subtype of a primitive data type. While primitive data types allow a range of values, literal narrows it down to specific predifined value (values in some cases).

For example:

```ts
let iamlit: "Hello"; //"Hello" is literal type

iamlit = "Hello"; //OK
iamlit = "Bounjor" //Error
```
Here `iamlit` can only have value of the literal.