---
id: z1lgwezpy12deg3225u4y33
title: At End
desc: ''
updated: 1709389540817
created: 1709369727516
---


## In the same array (fixed size)

1. Check if array has capacity
2. If yes, add the element to the array's length + 1
```js
function insertSorted(arr, n, key, capacity)
        if (n >= capacity)
            return n;
      
        arr[n] = key;
        return (n + 1);
    }
```

# Copy to a new array (dynamically sized)

```js
arr.push(new_element)
```

```python
def insertAtEnd():
    arr.append(new_element)
```