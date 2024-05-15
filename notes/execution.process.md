---
id: agm31jfpf7u95trbbk82clt
title: Process
desc: ''
updated: 1715183393997
created: 1713124712403
---


Process is a set of instructions.

- May or may not fail, but we don't rollback the entire process.
- Each process is allocated a seperate memory area      
- Process is heavyweight
- Cost of communication b/w processes is high
- Switching from one process to another takes some time
- Process is meaningful even if some of it is completed. 

Hence, process is never rolled back completely, but transaction is rolled back completely if it fails.
