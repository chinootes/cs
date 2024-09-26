

| [[paradigm.imperative]]                         | Declarative                  |
|------------------------------------|------------------------------|
| You say *how* to get what you want | You just say *what* you want |


## Declarative

```csharp
var results = collection.Where( num => num % 2 != 0);
```

Here we're saying:

=> Give everything where its odd.


Declarative and [[paradigm.func]] usually go hand-in-hand. For specifying _what_ you want, you usually need to paas a function as an argument, which requires [[paradigm.func.components.higher-order]]s. Some higher order functions are usually provided by languages which adhere to these paradigms, to express some common computation and iteration patterns.

Internally, these functions might iterate over the objects, where it is specified "how to do" something, but the key distinction lies in the usage in productive code, where you are declaring your demands.

These features and abstractions enable concise, expressive and maintainable code.