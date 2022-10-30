# Regex Tutorial

## What is Regular Expression or "regex"?

A regular expression is a pattern that is matched against a subject string from left to right. These expressions are extremely useful for extracting data like phone numbers, emails, etc., that follow a specific pattern from text. The term "regular expression" is usually referred to by an abbreviated term of "regex".

## Summary

In this tutorial, we will be exploring how to match a URL using regex. I will include the meta characters below. Click the table of contents to be taken to the particular meta character tutorial.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

- Anchors tell the regular expression where to start and end in the search. The `^` indicates that to match, a string which starts with whatever follows the carrot `^`. The `$` indicates the string ends with whatever was preceding it. When both are existing together, it indicates that the string MUST match whatever is in between `^` and `$` (an exact string match). In the expression provided, the entire collection of characters is wrapped in both a `^` and a `$` making the search exact.

### Quantifiers

- Quantifiers determine how many instances of a character, group, or character class can be present in the expression. This combination of characters has a few quantifiers. See the table of contents for more information on Groups, Capturing and Brackets.
- The `*` character will match anything it proceeds from zero to infinite times (depending on the number of occurances in the string). The third capture group: `([\/\w \.-]*)*`, searches for any instance of the criteria within the brackets, then as many instances of that criteria afterwards, including the possibility of no matches.
- The `+` matches one or more times, excluding zero times. In the capture group: `([\da-z\.-]+)`, the `+` will match any number of instances based off the declaration in square brackets, as long as it is at least once.
- The `?` matches zero or one time(s). The first capture group: `(https?:\/\/)?` will accept zero or one single instance of "s".
- The `{}` determines how many instances of the preceding group or character occur. `{2,6}` within the last capture group:
  `([a-z\.]{2,6})` searches for 2 to 6 instances of a character based off the criteria within the square brackets.

### Character Classes

- A character class defines a set of characters that can occur within the string.
- `\d` matches a single character that is a digit 0-9.
- `\w` matches any single word character such as "a-z", "A-Z", "0-9", and "\_".
- `\/` matches a single character of `/`.
- `\.` matches a single character of `.`.
