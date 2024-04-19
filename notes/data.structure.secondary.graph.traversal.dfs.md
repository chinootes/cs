---
id: n9rynktzsyif5sskvdctphr
title: Depth-first Search
desc: ''
updated: 1709137918093
created: 1709137855133
---

- Start at root node.
- Explore each branch as far as possible (till its depth).
- No more vertex left in that branch?
- Come back to where you can find vertices and start again.

Start - explore - backtrack - repeat.

![DFS](<../attachments/Depth-first Search (DFS)-image.png>)

## Preorder and Postorder DFS

- **Preorder**: When the node is "visited" while traversing to the depth.
- **Postorder**: When the node is "visited" once we have encountered the leaf node.

## Applications of DFS

- Cycle Detection
- Finding connected components
- Topological Sort
- Maze generation

## References

- [Depth First Search (DFS) Explained: Algorithm, Examples, and Code](https://youtu.be/PMMc4VsIacU?si=m7jEJLf80zjFGKAd)
