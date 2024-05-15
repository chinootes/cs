---
id: 1b96vabw8ua1z2fozxubnem
title: ACID
desc: ''
updated: 1715185811348
created: 1715185593747
---


A transaction should have the following properties:

- **Atomicity**: Either executed fully or none.
- **Consistency**: If database was consistent before transaction, it should remain consistent afterwards.
- **Isolation**: Logical isolation - two transactions shouldn't affect each other
- **Durability**: If a transaction is executed it should persist in the system irrespective of hardware/software failures.

$$$
    AID => C
$$$
