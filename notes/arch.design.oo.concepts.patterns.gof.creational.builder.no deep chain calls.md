---
id: 8ufija4foh4x7se3liqu4g2
title: Don't dig too deep in chain calls
desc: ''
updated: 1708779454214
created: 1708779437333
---

> Chain calls ko dil pe na lein.

Avoid digging to deep into collaborators while creating chain calls as it can risk exposing internals and cause other issues.

```cpp
*the dog should bark
dog->getHead( ) ->getMouth( ) -> getTongue( ) ->bark( ).
```

👆🏽Tight Coupling and dependencies

- Hard to change/extend
- No reuse of parts possible
- Hard to test

Solution

```cpp
dog->bark( ).
```
