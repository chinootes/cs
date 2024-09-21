---
id: x598wt0g2i71vrwvm1dt2qw
title: Searching
desc: ''
updated: 1726682963506
created: 1726682418436
---

## Binary Search

Here's the code using [[dev.algo.search.binary]] algorithm for searching an array:

```java
    public static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2;

            if (arr[mid] == target) {
                return mid;
            }

            if (arr[mid] < target) {
                left = mid + 1;
            }
            else {
                right = mid - 1;
            }
        }

        return -1;
    }
 ```