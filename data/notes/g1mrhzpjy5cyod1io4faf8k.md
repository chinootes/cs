
Java's implementation of [[os.memory.ram.user.stack]].


- Each thread has a private JVM stack created at same time as thread
  - Used to store data and partial results which will be needed while returning value for method and performing dynamic linking
- Stores [[os.memory.ram.user.stack.frame]]s
- References to objects stored here
