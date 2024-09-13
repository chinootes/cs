---
id: jik03wh5g5jxxfz2aklbmub
title: Multithreading
desc: ''
updated: 1725465662462
created: 1713121358159
---


## Creating a thread

Two ways-

1. extend [[lang.java.lib.classes.thread]] class
2. implement [[lang.java.lib.interfaces.runnable]] interface

Implement the `run()` method -> this is the code which will get executed when the thread runs.

## Executing Threads

- Call `start()` method

    The part after start method call is executed immediately. If you want to execute some part of the code after the thread execution, use `join()` method.

    ```java
        Thread thread = new ApnaThread();

        thread.start();

        //this part gets executed immediately after start() is called - while the thread is running

        thread.join();

        //this part gets executed after the thread execution is completed.
    ```

- Use [[lang.java.lib.interfaces.executor service]]

## Thread Execution



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
