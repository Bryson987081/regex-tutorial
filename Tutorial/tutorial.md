# Matching a Hex Value

Welcome, this is a guide on regular expressions or regex for short.  Regex can be used to validate many different things including emails, hex values, URLs, and HTML.  Ultimitley you learn how to understand patterns and principles of regex.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
In this tutorial we'll focus on hex values.  `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`  This is an example of what a regex looks like for a hex value.  Looks very confusing huh?  Don't worry, it's actuaclly a lot more simple than it looks!

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


### Regex Components
Let’s take a look the regex `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.


### Anchors
Anchors help define the start and end of the regex pattern:

- `^` - Asserts the position at the start of the string.

- `$` - Asserts the position at the end of the string.



### Quantifiers
Quantifiers specify how many times a pattern should be matched:

- `*` - Matches zero or more times.

- `+` - Matches one or more times.

- `?` - Matches zero or one time.

- `{n}` - Matches exactly n times.

- `{n,}` - Matches at least n times.

- `{n,x}` - Matches between n and x times.

In our example:

- `{6}` - Matches exactly 6 hexadecimal characters.

- `{3}` - Matches exactly 3 hexadecimal characters.


### Grouping Constructs
Grouping constructs allow for grouping multiple patterns, using parentheses `()`:

- `([a-f0-9]{6}|[a-f0-9]{3})` - This groups together the two possible patterns. Six hexadecimal characters or three hexadecimal characters.


### Bracket Expressions
Bracket expressions match a specific set of characters and are defined using square brackets `[]`:

- `[a-f]` - Matches any lowercase letter from a to f.

- `[A-F]` - Matches any uppercase letter from A to F.

- `[0-9]` - Matches any digit from 0 to 9.


### Character Classes
Character classes define a set of characters:

- `.`- Matches any character except newline.

- `\d` - Matches any digit.

    - `\D` - Matches any non-digit character.

- `\w` - Matches any alphanumeric character.

    - `\W` - Matches any non-alphanumeric character.

- `\s` - Matches any whitespace character.

    - `\S` - Matches any non-whitespace character.


### The OR Operator
The OR operator `|` allows for alternative patterns:

- `(a|b|c)` - Matches either a, b, or c.

- `[a-f0-9]{6}|[a-f0-9]{3}` - Matches either a six-digit or a three-digit hexadecimal color code.


### Flags
Flags modify the behavior of a regex pattern and are placed after the pattern:

- `i` - Case-insensitive matching.

- `g` - Global matching (find all matches).

- `m` - Multiline matching (treats input as multiple lines).


### Character Escapes
Character escapes interpret special characters literally, using a backslash \:

- `\#` - Ensures the `#` is treated as a literal character in patterns like `\#[a-f0-9]{6}`.


### Examples
Here are some examples of valid and invalid hex color codes:

- `#1E88E5` - Valid hex value
- `#FFFFFF` - Valid hex value
- `#ABC` - Valid hex value
- `#12_Z` - Invalid hex value


## Author

Feel free to checkout my GitHub [Bryson987081](https://github.com/Bryson987081)