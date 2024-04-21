---
id: prldrn4arpiwwudonbuj9jz
title: Thread Safety
desc: ''
updated: 1713648775236
created: 1713648406602
---

1. Stateless Implementation
    - Source of error in most cases (multithreaded apps)
        - Incorrectly sharing state between several threads
        - Don't make your methods rely on external state, nor maintain any state at all
2. Immutable Implementation
    - Need to share states between threads → make them immutable
    - Immutable classes = Thread safe
3. [[execution.concurrency.synchronization]]
