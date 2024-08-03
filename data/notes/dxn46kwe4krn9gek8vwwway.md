
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
