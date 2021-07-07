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

Quantifiers simply indicate a number of characters to match, or the length range of a set of characters that are being matched. In our example regular expression above:

```
([a-z\.]{2,6})
```

is referring to the top level domain(TLD) part of the e-mail address, i.e, the .com, .org, .edu. In this expression, we are looking for any string of characters that are letters between A and Z, where there are at least two and no more than six.

### Grouping Constructs

Grouping constructs are indicated by opening and closing parentheses, and they set off blocks of the regular expression as individual units apart from each other. In our regular expression example above, we have three grouped constructs:

```
([a-z0-9_\.-]+)
([\da-z\.-]+)
([a-z\.]{2,6})
```

The first group is referring to the username of the e-mail address, or the string coming before the @ symbol. The second is referring to the portion after the @ sign and before the ., i.e., yahoo, gmail, hotmail, etc. The third is the TLD mentioned in the Quantifiers section.

### Bracket Expressions

Bracket expressions define the allowed range of characters in that section of the string you are matching. In our regular expression example above, we again have three constructs:

 ```
 [a-z0-9_\.-]
 [\da-z\.-]
 [a-z\.]
 ```
 The first is saying that the section before the @ sign can include any letters a through z, any numbers 0-9, as well as a dot or a hyphen. The second is saying that the section following the @ sign can include ONE number followed by any letters a through z. The third is saying that the section can only contain letters a through z. 

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
