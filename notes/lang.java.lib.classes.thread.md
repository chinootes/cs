---
id: x80m51i2zu94y911j4pqc2g
title: Thread
desc: ''
updated: 1713122478926
created: 1713121833210
---

## Constants

- `NORM_PRIORITY` = 5 (Default priority)
- `MAX_PRIORITY` = 10
- `MIN_PRIORITY` = 1


## Methods

- [[lang.java.lib.interfaces.runnable]].`run()`
- `start()`: Starts thread execution - [[lang.java.jre.jvm]] calls `run()`
- `sleep(ms)`: Causes the thread to sleep for specified milliseconds.
- `join()`: Waits for the thread to die.
- `getPriority()`: Returns priority of thread
- `setPriority(int)`: changes priority of a thread
- [[lang.java.lib.classes.object]].`wait()`: stops the function until notified
- [[lang.java.lib.classes.object]].`notify()`: notifies other threads
