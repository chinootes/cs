---
id: 5mqyhqbl70k784qyd7mrkav
title: Thread Safety
desc: ''
updated: 1727368109520
created: 1713648406602
---

1. Stateless Implementation
    - Source of error in most cases (multithreaded apps)
        - Incorrectly sharing state between several threads
        - Don't make your methods rely on external state, nor maintain any state at all
2. Immutable Implementation
    - Need to share states between threads → make them immutable
    - [[arch.design.oo.patterns.immutable class]] = Thread safe
3. [[execution.concurrency.synchronization]]
