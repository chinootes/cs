
Lets say we want to find a value `target` in a data structure.

```pseudocode

BinarySearch(data_structure, target):
    left ← starting point of the data_structure
    right ← end point of the data_structure

    while left ≤ right:
        mid ← middle element of the data_structure between left and right

        if data_structure[mid] == target:
            return mid  // target found

        else if data_structure[mid] < target:
            left ← mid + 1  // search in the right half

        else:
            right ← mid - 1  // search in the left half

    return -1  // target not found

```