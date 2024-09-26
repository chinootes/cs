
Used to execute a `callback` function for all elements in ascending order.

## Parameters

### `callback` function

#### Arguments of the `callback` function

All three are _optional_.

- `element value`: The current value of the item.
- `element index`: The index of the current element being processed in the array.
- `array`: The array being iterated.

Note: These three arguments are optional.


### `thisObject`

An object to use as this when executing the callback.


## Example 

```ts
const fruits: string[] = ['Apple', 'Orange', 'Banana'];

// Example 1: Using all parameters
fruits.forEach((currentValue: string, index: number, arr: string[]) => {
    console.log(`Fruit at index ${index}: ${currentValue}`);
});

// Example 2: Using a custom 'this' value
const myObject = {
    greeting: 'Hello',
    displayFruit: function (fruit: string) {
        console.log(`${this.greeting}, ${fruit}!`);
    },
};

fruits.forEach(myObject.displayFruit, myObject);
```