---
id: qpf1s1uvtvs0mr8lwvyrgjg
title: G1
desc: ''
updated: 1713688527942
created: 1713687671569
---

# Garbage First 

Introduced in [[lang.java.v.9]] to [[lang.java.jre.jvm.gc.cms]]

- Operation
    - No concept of young and old generations
    - Divides Heap into several memory spaces
    - Collects from region which has most garbage → Garbage first (G1)
- Advantages
    - GC pauses can be tuned
    - Small pauses
    - Parallelism and concurrency together
    - Better heap utilisation