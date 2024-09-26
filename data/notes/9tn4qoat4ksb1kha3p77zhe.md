

`ExecutorService` is an interface which allows us to execute tasks on thread asynchronously


## Instantiation using `Executors` Factory class

Instance can be retrieved from `Executors` factory class using different factory methods based on the number and types of threads needed. 

### For single thread

```java
ExecutorService es = Executors.newSingleThreadExecutor();  
```

### For thread pool
    
```java
ExecutorService es = Executors.newFixedThreadPool(10); 
```    

### For scheduled thread pool
In scheduled thread pool, we can schedule tasks of the threads.

```java
ExecutorService es = Executors.newScheduledThreadPool(10); 
```

## Methods

### Executing Threads

```java
//We can use the following methods
execute(Runnable task)
submit(Runnable task) / submit(Callable<T> task)
invokeAny(Collection<? extends Callable<T>> tasks)
invokeAll(Collection<? extends Callable<T>> tasks);
```

### Shutting down

We can use the following methods after we're done. If we don't, the threads will keep running and JVM won't shut down.

- `shutdown()` method
- `shutdownNow()` method
- `awaitTermination()` method

