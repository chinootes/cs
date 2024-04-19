---
id: bbpcdgn1lwdxvief9kr3jkl
title: NodeJS
desc: ''
updated: 1709975579943
created: 1709667166008
---

NodeJS is based on Chrome's [[lang.js.v8]]. Initially, [[lang.js]] was intended for use in browser. In the browser, V8 was the compiler for JS. The creator of nodeJS simply made a runtime on top of this V8 engine.

Even though it is single-threaded, nodeJS still allows [[execution.async]] execution via [[paradigm.event driven]] architecture. It uses the [[paradigm.event driven.main loop]] or **event loop** to stay in the memory, while spinning up seperate worker threads for blocking operations. The threads are not created on-demand, but rather fetched from a [[arch.pattern.concurrency.thread pool]].

Non-blocking operations are executed in the main execution itself. The blocking operations are moved to an event queue.

## Flow of a request coming to a node JS server

```mermaid
sequenceDiagram
    Client      ->> Event Queue: Non-blocking request
    Event Loop  ->> Event Queue: New request aaya kya?
    Event Queue ->> Event Loop:  Yes
    Event Loop  ->> Event Loop:  Blocking hai ya non blocking?
    Event Loop  ->> Event Loop:  Non-Blocking
    Event Loop  ->> Event Loop:  Ye to main khud hi kar lunga

    Client      ->> Event Queue: Blocking request
    Event Loop  ->> Event Queue: New request aaya kya?
    Event Queue ->> Event Loop:  Yes
    Event Loop  ->> Event Loop:  Blocking hai ya non blocking?
    Event Loop  ->> Event Loop:  Blocking
    Event Loop  ->> Thread Pool: Dekh le bhai. Call karna fir
    Thread Pool ->> Event Loop: Ho gaya. Dekh lo
    Event Loop  ->> Event Loop:  Call back function    
```


