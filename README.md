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
