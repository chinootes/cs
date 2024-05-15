---
id: qaz8nexo7sxoz1a1fum03dw
title: Transaction
desc: ''
updated: 1715185850180
created: 1715183310524
---

Set of instruction which performs some logical work grouped into a single execution unit. If any task fails, the whole transaction fails. Therefore, a transaction is either successful or failure. There is no in between.

Both transaction and process are sets of instructions but a process is meaningful even if some of it is completed. Meanwhile, a transaction is a [[execution.process]] which has no meaning if half of it is completed. It is either completed or failed.

Hence, process is never rolled back completely, but transaction is rolled back completely if it fails.

## Transactions are performed on buffer

All operations in a transaction are performed on a buffer which is a copy of the database or record. So even if a transaction fails any stage, the buffer is removed and the database remains unaffected. If it is successful the data will be copied.


## Transaction States

- **Active**: Transaction is going on
- **Partially committed**: After R/W operations
- **Failure**: Can go to this state from Active or from partially committed.
- **Aborted**: The step after failure
- **Committed**: The step after partially committed if storing permanently is successful - no rollback from here.
- **Terminated**: Transaction ended.


## Result of Concurrent Transactions

- Waiting time 👇🏽
- Response time 👆🏽
- Resource Utilization 👆🏽
- Efficiency 👆🏽

## Dirty Read

When a transaction is allowed to read a row which is modified by another transaction but not yet commited, dirty read occurs.

Dirty read can result in wrong values in database if the first transaction's commit fails.
