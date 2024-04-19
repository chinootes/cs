---
id: fuigmwdwhm4hzh0gu75ypth
title: Deadlocks
desc: ''
updated: 1713125676278
created: 1713125639335
---

## Detection

Deadlocks are diffcult to detect as there are multiple locks and threads in Java which run even without us specifying.

### Detection using thread dumps

Use either of the following commands to ask the JVM to print info of all the threads running in the application.

Take the process ID of your application and run the following -

- `kill -3 12704` (where 12704 is the process ID)
- `jstack 11475 > ./out.txt` (will put that log in the specified file)

JVM will detect the deadlock itself and mention it.

### Detection using Java MXBean

MXBean is an API which you can run constantly in the background which can detect and tell you when the application goes into a deadlock state.

```java
private static void detectDeadlock(){
    ThreadMXBean threadBean = ManagementFactory.getThreadMXBean();
    long[] threadIds = threadBean.findDeadlockedThreads();
    boolean deadLock = threadIds != null && threadIds.length > 0;
    System.out.println("Deadlocks found: " + deadLock);
}
```

## Prevention

- Include timeout for your locks.
- Have a global order for locks
- Avoiding unnecessary and nested locks altogether
- Joining the threads