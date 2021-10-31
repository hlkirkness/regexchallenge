# Matching HEX Values with Regular Expressions

In this file, I will be explaining how a regular expression works. I will be focusing on matching HEX values.

## Summary

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The above regular expression is what we will be evaluating. It is used to match HEX values.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchor: ^ 
Code Snipet: `/^#`

Anchors show us what the beginning or end of the string has to look like. The ^ anchor means that the beginning of the string has to match the character #. This character is used to distinguish a hexidecimal number from a decimal number. The #, howeverm is optional.

Anchor: $
Code Snipet: `$/`

The $ is used to check if a string fully matches a pattern at the end of the string. The end of the string must match with the 3 or 6 character pattern that comes before the $ anchor.

### Quantifiers

Quantifier: ?
Code Snipet: `/^#?`

The ? implies a boolean value, either 0 or 1. This value makes the preceding character optional. In the case of our regex, the ? tells us that the character # (which is before the ?) is optional.

Quantifier: {}
Code Snipet: `[a-f0-9]{6}`
Code Snipet: `[a-f0-9]{3}`

This quantifier tells us how many times the previous pattern matches. Often times the quantifiers want the regex to match as many occurances of a particular pattern as possible. However, with the ? quantifier, the regex would match as few occurances as possible. In our regex, the quantifier is greedy.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)