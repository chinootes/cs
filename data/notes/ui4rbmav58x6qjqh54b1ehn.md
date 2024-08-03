
Technique to break [[concepts.dependency.cyclic]].

Whenever such a dependency is detected, a proxy or "early reference" is created for one of the entities is created before the full initialization and then load the dependency later lazily, resolving the dependencies.

