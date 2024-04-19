---
id: uqhl94rexh6xhzkz18gq1ua
title: Topological Sort
desc: ''
updated: 1709139717142
created: 1709139614567
---

It is a way of sorting a Directed Acyclic Graph in an order where for any edge $u \to v$, u always comes before v in the sort.

For a Topological Sort, the nodes should be executed in order of their direction.

- The nodes with no prerequisites (no arrows pointing towards them) are the leaf nodes.
- The leaf nodes come first in a postorder search and we trace back our steps from their.
- For a Topological Sort, the nodes with no prerequisites should be executed last.
- Since, the last node of topological sort is the first node of the postorder DFS traversal, and this order is maintained throughout the traversal => reversing postorder DFS automatically gives a topological sort for a Graph.

## References

[Depth First Search (DFS) Explained: Algorithm, Examples, and Code](https://youtu.be/PMMc4VsIacU?si=07x2kNfOdPjKJqoN)
