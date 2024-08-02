---
id: ui4rbmav58x6qjqh54b1ehn
title: Early Reference Resolution
desc: ''
updated: 1719760112590
created: 1719759934065
---

Technique to break [[concepts.dependency.cyclic]].

Whenever such a dependency is detected, a proxy or "early reference" is created for one of the entities is created before the full initialization and then load the dependency later lazily, resolving the dependencies.

