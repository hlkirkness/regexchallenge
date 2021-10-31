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
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

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

This quantifier tells us how many times the previous pattern matches. Often times the quantifiers want the regex to match as many occurances of a particular pattern as possible. However, with the ? quantifier, the regex would match as few occurances as possible. In our regex, the quantifier is greedy. The {6} in our regex implies that there are 6 instances of the string in the expression. This means the quantifier will allow 6 characters in the string that contain a-f and/or 0-9. The same would happen with a {3} but instead of 6 characters allowed, only 3 are.

### OR Operator

OR Operator: |
Code Snipet: `[a-f0-9]{6}|[a-f0-9]{3}`

The | is a boolean that can match the expression before or after it. In the case of our regex, the | will match with a 3 or 6 character string containing a-f and/or 0-9.

### Character Classes

Code Snipet: `a-f0-9`

Character classes will match one our of several characters that were defined in the set. A hyphen can define a range of characters and more than one can be used, such as in our code.

### Grouping and Capturing

Grouping and Capturing: ()
Code Snipet: `([a-f0-9]{6}|[a-f0-9]{3})`

The () groups the expression between them. This makes it so that multiple characters will appear as a single unit. This makes it so the data will be exposed as an array. 

### Bracket Expressions

Code Snipet: `[a-f0-9]`

Bracket expressions will match a specific pattern of characters defined within the brackets. A hyphen is used to show the range of characters (such as our a-f or 0-9).

### Greedy and Lazy Match

Code Snipet: `[a-f0-9]{6}`
Code Snipet: `[a-f0-9]{3}`
Quantifier: {}

Greedy means matching the longest possible string, whereas lazy means matching the shortest possible string. Normal quantifiers are greedy but when you apply the ? quantifier, it would become lazy and will match as few occurances as possible.

## Author

My name is Heather Kirkness. I am a student learning different web technologies with a goal of becoming a full stack web developer. Here is the link to my [GitHub](https://github.com/hlkirkness)