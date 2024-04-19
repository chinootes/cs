---
id: b64sk34fy5xp18ok43p5x7x
title: ExecutorService
desc: ''
updated: 1713125234893
created: 1713125223294
---

ExecutorService is an interface which allows us to execute tasks on thread asynchronously

## Instantiating

```java
ExecutorService executorService1 = Executors.newSingleThreadExecutor(); 
//Creates a ExecutorService object having a single thread.  
    
ExecutorService executorService2 = Executors.newFixedThreadPool(10); 
// Creates a //ExecutorService object having a pool of 10 threads.  
    
ExecutorService executorService3 = Executors.newScheduledThreadPool(10); 
//Creates a scheduled thread pool executor with 10 threads. 
//In scheduled thread pool, we can schedule tasks of the threads.
```

## Assigning Tasks

```java
//We can use the following methods
execute(Runnable task)
submit(Runnable task) / submit(Callable<T> task)
invokeAny(Collection<? extends Callable<T>> tasks)
invokeAll(Collection<? extends Callable<T>> tasks);
```

## Shutting down

We can use the following methods after we're done. If we don't, the threads will keep running and JVM won't shut down.

- shutdown() method
- shutdownNow() method
- awaitTermination() method

