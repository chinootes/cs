---
id: hmmx09b05y6dh6p06zp9qxw
title: Iterative Implementation of DFS
desc: ''
updated: 1709139913239
created: 1709138223075
---

```python
marked = [False] * G.size()
def dfs(G,v):
    stack = [v]
    while len(stack) > 0:
        v = stack.pop()
        if not marked[v]:
            visit(v)
            marked[v] = True
            for w in G.neighbours(v):
                if not marked[w]:
                    stack.append(w)
```

Time complexity: $O(V+E)$;
$V$ = no. of vertices
$E$ = no. of edges

- More generalizable and extensible than [[data.structure.secondary.graph.traversal.dfs.recursive]]. As in, it can be tweaked to incorporate other algorithms.
- Using Iterative Implementation, you can explicitly specify the stack size. While recursive approach uses the OS' default stack size, which is still typically small - and thus can cause stack overflow.
