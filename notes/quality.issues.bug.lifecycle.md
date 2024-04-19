---
id: 7zduynl98rxe103dc3b6xl0
title: Bug Lifecycle
desc: ''
updated: 1708455392602
created: 1708454746305
---

## Bug Workflow

```mermaid
flowchart TD
    1[1. Execute tests] --> 2[2. Record and submit a bug] 
    2 --> 3[3. Review and assign the bug]
    3 --> 4[4. Investigate and reproduce the bug]
    4 --> reproduced([Bug reproduced?])
    
    reproduced --Yes--> 5[5. Fix the bug]
    reproduced --No--> 6[6. Elaborate the bug]
    6 --> 4    

    5 --> 7[7. Verify the fix]
    7 --> fixed([Bug fixed])

    fixed --Yes--> 8[8. Close the bug]
    fixed --No--> 5
```
## Bug Life Cycle Stages

1. New/Open
2. Deferred/Postponed
3. Assigned
4. In Progress
5. Fixed
6. Pending Retest
7. Verified/Closed
8. Reopened

These stages can vary according to the organization and team.

## References

[What is Bug Life Cycle In Software Testing? Best Tools For Bug Management](https://katalon.com/resources-center/blog/bug-defect-life-cycle)
