
Many times in algorithmic problems, we want to store state against a `key` value. An obvious way which comes to mind is using a hashmap. But there can be multiple ways of doing it. 

## Ways to map key-value

### 1. Hashmap/dictionary (key-value data structures)

Values(state) which you want to maintain can simply be stored against a `key` in such data structures.

💡In addition to identifying if an element _exists_ in a dataset, hashmaps can also be used to identify if the dataset contains any duplicate simply by comparing the size of hashmap with the original dataset.

```js
var containsDuplicate = (nums) =>new Set(nums).size != nums.length;
```

### 2. Array

While not the first thing which comes to mind when thinking of a key-value pairs, arrays can be used in cases where the number of keys are going to be limited. 

For example, in cases where the `key`s are ASCII characters, you can simply create an array of size 256 and store the state against the index corresponding to ASCII value of the character in the array. 

If keys are alphabets, the array size would be 129.

### 3. BITs