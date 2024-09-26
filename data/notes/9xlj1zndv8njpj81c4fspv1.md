
Used for pattern matching in string. Common use cases include text validation and text search.

Regexes are enclosed within `/ /` (this document doesn't use these enclosings in most regexes to keep it clean).

## Some common ones 

- `[abc]` - a, b or c
- `[^abc]` -  any character except a, b, c
- `[a-z]` - a to z
- `[A-Z]` - A to Z
- `[a-zA-Z]` - a to z, A to Z
- `[0-9]` - 0 to 9

## Flags

- `g`

    `/a/` will only match the first occurence of a.
    `/a/g` will match all occurences of a throughout the string.

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
- `.` - any character except a newline

## Escaping

Use `\` to replace any special character.


## Logical Operators

- `^` - Negation
- `|` - Logical OR
- `()` - to group your logic


## Standards

Regular expressions (regex) are not defined by a single, universally accepted standard like an RFC. However, there are efforts to establish some level of consistency across different regex implementations. 

Some regex standards are:

- POSIX Basic Regular Expressions (BRE)
- Extended Regular Expressions (ERE)
- PCRE (Perl Compatible Regular Expressions)
- I-Regexp (RFC 9485) 


## References

- [Regular expression syntax cheat sheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet)

- Good concise videos
    - [REGEX (REGULAR EXPRESSIONS) WITH EXAMPLES IN DETAIL | Regex Tutorial](https://www.youtube.com/watch?v=9RksQ5YT7FM&ab_channel=CrackConcepts)
    - [Regular Expressions (RegEx) in 100 Seconds - Fireship - YouTube](https://www.youtube.com/watch?v=sXQxhojSdZM&ab_channel=Fireship)