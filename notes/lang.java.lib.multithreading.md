---
id: 2yvl1jdxsuy6584xzcm4759
title: Multithreading
desc: ''
updated: 1727375344580
created: 1727373800483
---

### Creating a thread

Two ways-

1. extend [[lang.java.lib.multithreading.thread]] class
2. implement [[lang.java.lib.multithreading.runnable]] interface

Implement the `run()` method -> this is the code which will get executed when the thread runs.

### Executing Threads

- Call `start()` method

    The part after start method call is executed immediately. If you want to execute some part of the code after the thread execution, use `join()` method.

    ```java
        Thread thread = new ApnaThread();

        thread.start();

        //this part gets executed immediately after start() is called - while the thread is running

        thread.join();

        //this part gets executed after the thread execution is completed.
    ```

- Use [[lang.java.lib.multithreading.executor service]]