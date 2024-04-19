---
id: rxnpk3j7odz9k9srpmquvz5
title: Imperative 
desc: ''
updated: 1709733499247
created: 1708622041376
---

| Imperative                         | [[paradigm.declarative]]                  |
|------------------------------------|------------------------------|
| You say *how* to get what you want | You just say *what* you want |

## Imperative

```csharp
List<int> results = new List<int>();
foreach(var num in collection)
{
    if (num % 2 != 0)
          results.Add(num);
}
```

Here, we're saying:

1. Create a result collection
2. Step through each number in collection
3. Check the number. If its odd, add it to the results
