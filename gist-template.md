# Expressions Tutorial

This tutorial will explain how specific regular expression, or regex, functions, detailing parts of the expression and describing what each part does.

## Summary

The tutorial will provide details about the below regex patterns...
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/i

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
^ signifies beginning of the string
$ signifies the end of the string

### Quantifiers
+ after [a-z0-9_\.-] and [\da-z\.-] means "one or more" of the preceding characters or digits
{2,6} specifies that the top-level, rightmost segment, domain must be between 2 and 6 characters long

### Grouping Constructs
([a-z0-9_\.-]+) - captures the username portion
([\da-z\.-]+) - captures the domain name
([a-z\.]{2,6}) - captures the top-level domain

### Bracket Expressions
[a-z0-9_\.-] allows lowercase letters, numbers, underscores, dots, and hyphens in the username
[\da-z\.-] allows digits, lowercase letters, dots, and hyphens in the domain name
[a-z\.] allows lowercase letters and dots in the top-level domain

### Character Classes
a-z matches any lowercase letter
0-9 and \d match any digit
\. matches a literal dot
- matches a hyphen
_ matches an underscore

### The OR Operator
This regex doesn't use the OR operator (|), as the bracket expressions provide the necessary character alternatives.

### Flags
i makes the pattern case-insensitive, allowing both upper and lowercase letters
u enables Unicode (multiple language) support


### Character Escapes
\. escapes the dot character to match character or number litterally with the backslash in front

## Author
Tracey Litschgi