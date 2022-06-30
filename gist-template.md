# Tutorial on the use of regular expressions or regex.

This is tutorial on the use of regular expressions (regex).  A regular expression is a group of characters that defines a search pattern. This tutorial will walk you through a regex and explain what each symbol represents and how it works in the matching of possible patterns.

## Summary

You will learn through the following example how to create a regular expression that can identify urls.  In this tutorial we will break the regex into groupings and define how each group matches a possible pattern. 

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

First Captureing Group:

`(https?:\/\/)?`
- `? matches the previous token between zero and one times, as many times as possible.`
- `http matches the characters http (case sensitive)`
- `h matches the character h (case sensitive)`
- `t matches the character t (case sensitive)`
- `t matches the character t (case sensitive)`
- `p matches the character p (case sensitive)`-`s matches the character s (case sensitive)`
- `? matches the previous token between zero and one times, as many times as possible.`
- `: matches the character :`
- `\/ matches the character /`
- `\/ matches the character /`

Second Capturing Group:

`([\da-z\.-]+)`
- `Match a single character present in the list below [\da-z\.-]`
- `+ matches the previous token between one and unlimited times, as many times as possible.`
- `\d matches a digit (equivalent to [0-9])`
- `a-z matches a single character in the range between a and z (case sensitive)`
- `\. matches the character .`
- `- matches the character -`
- `\. matches the character .`

Thid Capturing Group:

`([a-z\.]{2,6})`
- `Match a single character present in the list below [a-z\.]`
- `{2,6} matches the previous token between 2 and 6 times, as many times as possible`
- `a-z matches a single character in the range between a and z (case sensitive)`
- `\. matches the character .`

Fourth Capturing Group:

`([\/\w \.-]*)*`
- `* matches the previous token between zero and unlimited times, as many times as possible.`
- `A repeated capturing group will only capture the last iteration. Put a capturing group around the repeated group to capture all iterations or use a non-capturing group instead if you're not interested in the data`
- `Match a single character present in the list below [\/\w \.-]`
- `* matches the previous token between zero and unlimited times, as many times as possible.`
- `\/ matches the character /`
- `\w matches any word character (equivalent to [a-zA-Z0-9_]) (case sensitive)`
- `\. matches the character .`
- `- matches the character -`
- `\/ matches the character /`
- `? matches the previous token between zero and one times, as many times as possible.`
- `$ asserts position at the end of the string, or before the line terminator right at the end of the string.`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)

## Regex Components
The / that contain the regex make the expression a literal.
- `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### Anchors
The two characters below are the anchors of the regular expression.
- `^ Indicates that the match must be at the begining of the string`
- `$ asserts position at the end of the string, or before the line terminator right at the end of the string`

### Quantifiers
Quantifiers determine how many times a pattern in matched.
- `? May include zero or one occurances of the preceding element which would be any letter or number.`
- `+ Matches the previous token one or more times.`
- `* Matches the previous token between zero and unlimited times, as many times as possible.`
- `The {} sets limits for the match in this regex the limit is set between 2 and 6 times.`

### Character Classes
These are the bracket expressions.  They determine the charaters or the range of characters for the matching pattern.
- `[\da-z\.-] Match a single digit (d) 0 - 9 or letter a to z and a literal - to follow.` 

### Grouping and Capturing
Group the different componets of the string makes certain to check that the requirements are satisfied.
- `(https?:\/\/)?`
- `([\da-z\.-]+)`
- `([a-z\.]{2,6})`
- `([\/\w \.-]*)*`

### Bracket Expressions
Bracket expressions can be used to match allowable characters. Anything inside of the set of square brackets ([]) will represent the chararcters that are being matched. 
- `[\da-z\.-] Match a single digit (d) 0 - 9 or letter a to z and a literal - to follow.` 
- `[a-z\.] Match a single letter from a to z.`
- `[\/\w \.-] Match a single word (w) and the literal - to follow.`

### Character Escapes
The email regex tutorial contains two types of character escapes: `\.` and `\d`. `\.` indicates this is a literal `.` instead of the wildcard character class. `\d` matches any of the numbers 0-9 and is simply used to represent a digit. 

## Author
I can be reached at chris.borer@gmail.com

View my GitHub Profile: [cspower5](https://github.com/cspower5)