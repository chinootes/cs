---
id: sddclm7ri93aa3o3ny6a32x
title: Recursive Implementation of DFS
desc: ''
updated: 1709138255882
created: 1709138098108
---


```python
def dfs(G,v):
    visit(v)
    for w in G.neighbours(v):
        dfs(G,w)
```

The only issue in the above algorithm is that we'll end up visiting nodes we have already visited. Thus, we need to mark the already visited nodes.

```python
marked = [False] * G.size()
def dfs(G,v):
    visit(v)
    marked[v] = True
    for w in G.neighbours(v):
        if not marked[w]:
            dfs(G,w)
```

Time complexity: $O(V+E)$;
$V$ = no. of vertices
$E$ = no. of edges

Cleaner and more readable than [[data.structure.secondary.graph.traversal.dfs.iterative]].

## Implementation for Postorder DFS

Just move the visit() call to the end.

```python
marked = [False] * G.size()
def dfs(G,v):
    marked[v] = True
    for w in G.neighbours(v):
        if not marked[w]:
            dfs(G,w)
    visit(v)
```