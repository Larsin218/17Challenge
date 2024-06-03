# Regex Tutorial

In this tutorial, you will be given a general understanding on what a regex is, an example of one, and how it works.

## Summary

Here is a regex used for matching a hex value: `^#?([a-f0-9]{6}|[a-f0-9]{3})$`. This pattern checks the input for a string that can optionally start with a `#`, followed by either six or three hexadecimal digits. At first, it looks incomprehensible. However, there are a few giveaways as to how this regex is structured and how you can read it.
We will analyze some of the individual parts of this regex in order to get a better understanding of the overall pattern.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

Anchors are used to match positions within a string. The anchors used in this regex are `^` and `$`. The `^` anchor defines where the start of the string is. It is important to keep in mind that every regex is case sensitive.
As an example, we will take the string `"Hello World"`. The `^` will start at `"Hello"` and see everything after that. As previously stated, every regex is case sensitive, so `"Hello"` and `"hello"` will not match. This only applies to the first part of the string, however, so `"Hello"` and `"Hello world"` would match.
The `$` anchor defines where the end of the string is. This means that everything after "World" will not be seen.

### Quantifiers

Quantifiers set limits on the input. We are using `?` and `{}`. `?` is used to specify if something matches the pattern either zero or one time. `{}` is used to match the pattern a certain amount of times. In our regex, `{6}` and `{3}` mean that we are looking for exactly 6 or 3 characters.

### Grouping Constructs

Grouping constructs are used to check multiple parts of a regex. In other words, it allows for multiple filters to be used at once. We use `()` to house the different filters of the regex.

### Bracket Expressions

Bracket Expressions define characters to look for. `[]` this is how we use them. In our regex, we are looking for hexadecimal digits. These consist of the numbers 0-9 and letters a-f, which are considered digits in hexadecimal. So, to use these expressions, we write `[a-f0-9]` to ensure that the matches found only consist of hexadecimal digits.

### Character Classes

Character Classes are used to define the specific characters that we look for. As stated in the bracket expression section, we are looking for hexadecimal digits (`0-9` and `a-f`). These is considered a character class because we are setting specific parameters for what can be accepted as a match.

### The OR Operator

The OR operator is used to set two different sets of limits on the input. `|` this is what it lookes like. For example, we use it in our regex to look for a 6 digit value OR a 3 digit value.

## Author

This tutorial was made by Luke Smith, a student majoring in computer science, aspiring to become a full stack web developer. Here is a link to my GitHub profile for further questions/comments.
