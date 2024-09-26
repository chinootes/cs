
Functions without a name. 

There are different ways of creating anonymous functions:

```js
// An anonymous function assigned to a variable
const add = function(x, y) {
    return x + y;
};
console.log(add(2, 3));  // Output: 5

// An anonymous function used as a callback
setTimeout(function() {
    console.log("Hello, World!");
}, 1000);

```

Can be created using [[paradigm.func.components.lambda]] expressions. Such functions are called lambda functions.

```python
# Anonymous (lambda) function passed to map
squared = list(map(lambda x: x ** 2, [1, 2, 3, 4]))
print(squared)  # Output: [1, 4, 9, 16]

```


