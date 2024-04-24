---
id: a7dyttdu6xtjr6zv3q205we
title: Regex
desc: 'Regular Expressions'
updated: 1713975845568
created: 1713974732773
---

Used for pattern matching in string. Common use cases include text validation and text search.

- `[abc]` - a, b or c
- `[^abc]` -  any character except a, b, c
- `[a-z]` - a to z
- `[A-Z]` - A to Z
- `[a-zA-Z]` - a to z, A to Z
- `[0-9]` - 0 to 9

## Quantifiers

- `[ ]?` - occurs 0 or 1 times
- `[ ]+` - occurs 1 or more times
- `[ ]*` - occurs 0 or more times
- `[ ]{n}` - occurs n times
- `[ ]{n,}` - occurs n or more times
- `[ ]{y,z}` - occurs at least y times but less than z times

## Metacharacters

- `\d` - all digits ≍ `[0-9]`
- `\w` - all "word" (alphanumeric) characters ≍  `[a-zA-Z0-9]`
- `\D` - everything except digits ≍ `[^0-9]`
- `\W` - everything except alphanumeric characters ≍ `[^a-z]`

## Escaping

Use `\` to replace any special character.


## Logical Operators

- `^` - Negation
- `|` - Logical OR
- `()` - to group your logic


## References

- [Regular expression syntax cheat sheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet)

- Good concise videos
    - [REGEX (REGULAR EXPRESSIONS) WITH EXAMPLES IN DETAIL | Regex Tutorial](https://www.youtube.com/watch?v=9RksQ5YT7FM&ab_channel=CrackConcepts)
    - [Regular Expressions (RegEx) in 100 Seconds - Fireship - YouTube](https://www.youtube.com/watch?v=sXQxhojSdZM&ab_channel=Fireship)