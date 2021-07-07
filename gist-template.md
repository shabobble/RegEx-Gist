# Regular Expressions - Email Validation

Regular expressions are a great method for performing validation in your code without relying on an external library, and are becoming increasingly popular recently. They can look a bit arcane from the outside, but understanding them is worth the read.

## Summary

A popular use for regular expressions is to validate that a provided string is an e-mail address. Such an expression may look like this: 

```
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
```

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

The characters ^ and $ are start-of-line and end-of-line anchors recently. By putting ^ before a character, you are saying the first character in your string must match that character and by putting a $ after a character you are saying that the last character in your string must match that character. In our regular expression above, by enclosing the entire thing between ^ and $, we are saying that the regular expression must match the entire string.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
