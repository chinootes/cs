---
id: v67rl38x8m03qayrtpvnz1n
title: Optional
desc: ''
updated: 1727016426223
created: 1727015260517
---

- Represents a value that may or may not be present.
- Useful for handling situations where a value might be null, preventing [[dev.issues.exception.types.unchecked.null pointer]]s.


## Usage

```java
  public void box(Cat schrodingers){
    Optional<String> optionalName = Optional.ofNullable(schrodingers);

    if (optionalName.isPresent()) {
        System.out.println("Cat is alive");
    } else {
        System.out.println("Cat is dead");
    }
  }
```