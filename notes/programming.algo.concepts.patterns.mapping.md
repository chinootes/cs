---
id: 7qlj3vnx3e1orrhxu0zm1qk
title: Mapping
desc: ''
updated: 1712079035522
created: 1712078506545
---

Many times in algorithmic problems, we want to store state against a `key` value. An obvious way which comes to mind is using a hashmap. But there can be multiple ways of doing it. 

# Ways to map key-value

## 1. Hashmap/dictionary (key-value data structures)

Values(state) which you want to maintain can simply be stored against a `key` in such data structures.

## 2. Array

While not the first thing which comes to mind when thinking of a key-value pairs, arrays can be used in cases where the number of keys are going to be limited. 

For example, in cases where the `key`s are ASCII characters, you can simply create an array of size 256 and store the state against the index corresponding to ASCII value of the character in the array. 

## 3. BITs