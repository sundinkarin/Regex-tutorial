# Regex Explained

In JavaScript you can sort direct matches using the literal meaning of the keys. To make a more usefull encompassing search you can use a regular expression - also known as a regex. Regex are universal and can be used within all programming languages. 

## Summary

The regex below is used to match an HTML tag. This allows you to make sure the input from a field validates the correct format for an HTML tag.

Matching an HTML Tag  /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

`/` Open - the start of a Regex or regular expression.
`^` Start - beginning of a string or line.
`<` means less than.
`>` means greater than.
`()` capturing a group of symbols.
`[]` a range of characters that you want to match.
`+` quantifier tells you how many of the previous characters will be repeated.
`[^]` Negated set - symbols that you don't match in a set.
`*` quantifier tells you to match zero or more symbols.
`?:` Non capturing group. Where you check for a match but you don't save the symbols.
`.` matches any character except line breaks.
`|` Alternation. Acts like a boolean OR.
`\s` Whitespace - spaces, tabs, line breaks.
`$` End of the string or end of the line.
`/` Close - the end of a regular expression and the start of expression flags.

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
The regex components are listed below.

### Anchors
The `^` anchor signifies a string that begins with the characters that follow it. In all cases the regex is case sensitive. It can be done in two ways. First is an exact match of characters and spaces. The second way to match is with a range of matches using bracket expressions.

In the expression up above...

### Quantifiers
Quantifiers often include the minimum and maximum regex that you are searcching for.  

### OR Operator
`a(b|c)`     matches a string that has a followed by `b` or `c` (and captures `b` or `c`) `->`
`a[bc]`      same as previous, but without capturing` b` or `c`

### Character Classes
Distinguish different types of characters, between letters and digits.

### Flags
 Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. The three most common flags are:
    `g` Global search
    `i` Case-insensitive search
    `m` Multi-line search

### Grouping and Capturing
You group together regex by using parenthesis `()`. Between two sets of subexprssions you would  use the colon `:`. If you group constructs you have two primary categories, these are capturing and non-capturing.

### Bracket Expressions
A range of characters to be matched are set inside square brackets `[]`. We can also call these positive character group because they are inclusive of what we want to search for.
`*` matches the pattern 0 or more times.
`+` matches the pattern 1 or more times.
`?` matches the pattern 0 or 1 time.
`{}` there are 3 ways to use these brackets
    `{n}` exact match `n` number of times
    `{n,}` matches at least `n` number of times
    `{n, x}` matches from a minimum of `n` to a maximum of `x`

### Greedy and Lazy Match
The quantifiers are greedy and find all occurences of the pattern. but if you add a `?` at the end it finds the least number of occurences possible.

### Boundaries
`\b` represents an anchor like caret (it is similar to `$` and `^`) matching positions where one side is a word character (like \w) and the other side is not a word character (for instance it may be the beginning of the string or a space character).

It comes with its negation, `\B`. This matches all positions where `\b` doesn’t match and could be if we want to find a search pattern fully surrounded by word characters.

### Back-references
Backreferences refer to a previously captured group in the same regular expression.

### Look-ahead and Look-behind
`d(?=r)`       matches a `d` only if is followed by `r`, but `r` will not be part of the overall regex match `->`
`(?<=r)d`      matches a `d` only if is preceded by an `r`, but `r` will not be part of the overall regex match `->`

## Author
Karin is a Jr. Web Developer currently enrolled in a Full Stack Web Program with Carleton University.
 https://github.com/sundinkarin/
