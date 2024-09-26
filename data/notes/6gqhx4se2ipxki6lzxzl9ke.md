
Any algorithm involving use of two pointers/index variables to traverse over a data structure.

You take two pointers and move them untill you find the expected result.

There are many variants of this approach since the approach is only about taking two pointers. It only gets more concrete when we dig deeper.

Categorizing on basis of how the pointers move:

1. Running from both ends of an array
2. Slow & Fast Pointers
3. Running from beginning of 2 arrays / Merging 2 arrays
4. Split & Merge of an array / Divide & Conquer

## Slow and fast pointers

Specific pattern of two pointer algorithms where one pointer moves faster than the other. 

The movement of fast could be n times that of the slow pointer, where n is any positive integer. Or the slow pointer could be started late from the first node. 

### Use cases

1. **To detect cycle in a linked list**: If there is a circular track and one car is moving faster than the other, the two cars are bound to cross at some point.
2. **To find middle element of a list**: When the fast pointer going at 2x of slow pointer reaches the end - slow pointer will be at the middle element of the list.
3. **To find $$n^{th}$$ element from the end in a list**: Start the slow pointer once the fast pointer reaches the $$n^{th}$$ element and then move both at the same speed. By the time, the fast pointer reaches the end, slow pointer will be at nth element from the end.

## References

- [Solved all two pointers problems in 100 days - Leetcode discuss](https://leetcode.com/discuss/study-guide/1688903/Solved-all-two-pointers-problems-in-100-days)