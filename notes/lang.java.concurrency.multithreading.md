---
id: jykhz7pwchhdipdk9bluyqp
title: Multithreading
desc: ''
updated: 1713125620725
created: 1713121358159
---

## Creating a thread

Two ways-

1. extend [[lang.java.lib.classes.thread]] class
2. implement [[lang.java.lib.interfaces.runnable]] interface

Implement the `run()` method.

## Executing Threads

- Use `start()` method
- Use [[lang.java.lib.interfaces.executor service]]

## Java Thread Life Cycle
```mermaid
flowchart LR
    subgraph Thread
        New--start called--> Runnable
        Runnable-->Running
        Running  --run method exits or stop method called-->Terminated
    end
    subgraph Blocked Code
        Non-runnable --sleep done, I/O complete, lock available, resume, notify, notifyAll--> Runnable
        Running --sleep, block on I/O, wait for lock, suspend, wait--> Non-runnable
    end
```

## Thread Scheduler

Task executes for a predefined slice of time and then re-enters pool of ready tasks.

Next task decided based on priority and other factors.

Uses [[execution.scheduling.pre-emptive]] and [[execution.scheduling.time slicing]]
