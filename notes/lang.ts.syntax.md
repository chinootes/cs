---
id: qo4mtkjc1mpo8xcrhbhqrnr
title: Syntax
desc: ''
updated: 1714073646294
created: 1713886095577
---


## Hello World

```ts
console.log("Hello world!");
```

## Rules

## Naming Conventions

## Comments

```ts
//Single line comment

/* Multi 
 line 
 comment */
 
```
## Variables 

### Declaration

```ts
    let x;
    
    // with type
    let x: number; //types are specified using type annotations
```
### Initialization

```ts
    x = true // type-automatically inferred as boolean
    x = 123; //compile-time error
```
### Both at once

```ts
    let x = true // type-automatically inferred as boolean
    x = 123; //compile-time error
```

## Constants

```ts
    const PI = 3.14;
    const PI = 3.14;
```

## Data types

### Primitives

- `string`
- `number`: No int or float. Every number is simply `number`.
- `boolean`

💡The type names String, Number, and Boolean (starting with capital letters) are legal, but refer to some special built-in types that will very rarely appear in your code. Always use string, number, or boolean for types.

- `any`: Special type which you can use whenever you don't want a particular value to cause typechecking errors.

    ```ts
    let obj: any = { x: 0 };
    // None of the following lines of code will throw compiler errors.
    // Using `any` disables all further type checking, and it is assumed
    // you know the environment better than TypeScript.
    obj.foo();
    obj();
    obj.bar = 100;
    obj = "hello";
    const n: number = obj;
    ```

    Can be disabled by setting `noImplicitAny` flag in [[lang.ts.config]] 
    

### Compound
 
#### Array

##### Declaration

```ts
let x: number[]
```

```ts
Array<number> arr;
```

##### Initialization

```ts
x = [1,2,3] // type inferred as Array
```
##### Both at once

```ts
let x = [1,2,3] // type inferred as Array
```

#### Strings

```ts
 let gina: string;
 gina = "boyle";

 let holt = "kevin"; // type inferred as string
```

#### Objects (kind of like structures)

```ts
// The parameter's type annotation is an object type
function printCoord(pt: { x: number; y: number }) { // here the type of pt is defined as composed of x and y

  console.log("The coordinate's x value is " + pt.x);
  console.log("The coordinate's y value is " + pt.y);
}
printCoord({ x: 3, y: 7 });
```

##### Optional properties

```ts
function printName(obj: { first: string; last?: string }) {
  // ...
}
// Both OK
printName({ first: "Bob" });
printName({ first: "Alice", last: "Alisson" });
```

Checking for `undefined` mandatory for optional properties

```ts
function printName(obj: { first: string; last?: string }) {
  
  // Error - might crash if 'obj.last' wasn't provided!
  console.log(obj.last.toUpperCase()); //'obj.last' is possibly 'undefined'.

  if (obj.last !== undefined) {
    console.log(obj.last.toUpperCase());
  }
 
  //modern JavaScript syntax:
  console.log(obj.last?.toUpperCase());
}
```
#### Union Types

Combination of multiple types. Union type basically says that a variable/parameter can be either of the types within the union.

```ts
function printId(id: number | string) {
  console.log("Your ID is: " + id);
}
// OK
printId(101);
// OK
printId("202");
// Error
printId({ myID: 22342 });
```

Any operation on such parameter/variable will only work if the operation is valid for both all types in the union.

```ts
function printId(id: number | string) {
  console.log(id.toUpperCase()); //Error - method not applicable for number

//Solution to this - narrow down the type
  if (typeof id === "string") {
    // In this branch, id is of type 'string'
    console.log(id.toUpperCase());
  } else {
    // Here, id is of type 'number'
    console.log(id);
  }
}
```
💡It might be confusing that a union of types appears to have the intersection of those types’ properties. This is not an accident - the name union comes from type theory. The union number | string is composed by taking the union of the values from each type. Notice that given two sets with corresponding facts about each set, only the intersection of those facts applies to the union of the sets themselves. For example, if we had a room of tall people wearing hats, and another room of Spanish speakers wearing hats, after combining those rooms, the only thing we know about every person is that they must be wearing a hat.

#### Type Aliases

```ts
// For object types
type Point = {
  x: number;
  y: number;
};

//For union types
type ID = number | string;

// For primitive - Unnecessary but legal
type UserInputString = string;
```

#### Interfaces

```ts
interface Point {
  x: number;
  y: number;
}
```

#### Classes

##### Creating objects

##### Using objects



## Operators

## Flow

### Conditionals

### Loops

#### Traditional 

```ts
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```

#### for...of

Loops on elements.
```ts
for (let index of fruits) {
    console.log(fruits[index]);
}
```

#### for...in

Loops on indexes/keys.
```ts
for (let index in fruits) {
    console.log(fruits[index]);
}
```

💡 You'd think that `index` will be a `number`, but no, index here is a `string`. What's more? You can access elements using this index (as showm above), because its converted by [[type theory.casting.implicit]]. But if you use it to initialize another variable, like `j=i+1`, you can't use `j` as a `number`, `j` will also be a `string`. Weird stuff.

So prefer for..of or traditional for loop for arrays. Use for..in for things like Maps.


## Functions/Methods

### Parameter type annotation

```ts
function greet(name: string) {
  console.log("Hello" name.toUpperCase() + "!!");
}
```

### Return type annotation

```ts
function getFavoriteNumber(): number {
  return 26;
}
```

### Functions which return Promises

```ts
async function getFavoriteNumber(): Promise<number> {
  return 26;
}
```

### Anonymous functions

```ts
const names = ["Alice", "Bob", "Eve"];

//using function keyword
names.forEach(function (s) {
  console.log(s.toUpperCase());
});
 
// Arrow functions
names.forEach((s) => {
  console.log(s.toUpperCase());
});

```

### main



