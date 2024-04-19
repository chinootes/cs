---
id: 31v0sasm45sr0g8ff2df7ty
title: Representating Graphs
desc: ''
updated: 1709139797096
created: 1708969946105
---

```mermaid
graph LR
    0((0)) --- 1((1))    
    0((0)) --- 2((2))
    1((1)) --- 3((3))            
    0((0)) --- 3((3))
    2((2)) --- 3((3))
    3((3)) --- 4((4))                      
```

## Adjacency Matrix

$$
A_{ij} =     1  \;\;\; if \ edge(i,j) \\
\;\;\;\;\;\; 0  \;\;\; otherwise 
$$


|      | 0 | 1 | 2 | 3 | 4 |
|----------------------|
 **0** | 0 | 1 | 1 | 1 | 0 |
 **1** | 1 | 0 | 0 | 1 | 0 |
 **2** | 1 | 0 | 0 | 1 | 0 |
 **3** | 0 | 1 | 1 | 0 | 1 |
 **4** | 0 | 0 | 0 | 0 | 1 |


## Edge Set

$$
E = \{(0,1), (0,2), (0,3), (1,3), (2,3), (3,4)\}
$$


Harder to extract information about vertices of the graph => Not that common.


## Adjacency List

```mermaid
graph LR
    Node0[0] --> List0[1 , 2]
    Node1[1] --> List1[0 , 3]
    Node2[2] --> List2[0 , 3]
    Node3[3] --> List3[0, 1, 2, 4]
    Node4[4] --> List4[3]    
```

- Easy access to neighbours of a node -- useful in graph algorithms.
- Most real world graphs are sparse. That is, large number of nodes with fewer number of edges. For example, in a social network, there could be billions of people (nodes), but each person (node) will only have thousands of edges at most.
