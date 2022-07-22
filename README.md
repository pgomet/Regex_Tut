# Regex Tutorial

A collection of patterns known as a regular expression, or regex for short, can be used to examine character combinations in strings. 

Regex can be used to find patterns of characters within a string, to find/replace certain characters or a specific sequence of characters within a string, or just as a brain-teaser puzzle.

Regex is most frequently used to validate user input. Email addresses, usernames, URLs, HTML tags, and more are a few examples.

In this following lesson, I'll describe the various elements of the email validation regular expression (regex).

## Summary

In this tutorial, we'll look at a regex that may be applied to validate an email. Please refer to the regex below.

* `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

You could find that the regex resembles an ordinary email address if you look at it carefully. See the differences below.

* `([a-z0-9_\.-]+)` + `@` + `([\da-z\.-]+)` + `\.([a-z\.]{2,6})`
* `bob (username)` + `@` + `gmail (server name)` + `.com (top-level domain)`

Let's examine the meanings of each character now that we can notice the commonalities.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

The following elements are included in this regex:

- Character set matching
- Matching fields and groupings

### Anchors

* Regex can match a position such as before, after, or between characters thanks to anchors. The `^` and `$` anchors are essentially used to mark the before and after of the regex in the email. This establishes where the regex match will appear.

### Quantifiers

* A regex can determine the number of characters or expressions it needs to match due to quantifiers. We have two quantifiers in our regex: `+` and `{}`.

    * The `+` instructs the regex to repeatedly match the item.
    * the `{}` requests that the regex match "n" occurrences of the preceding item ("x"). This is expressed as follows: x n. In our regex this is used for `[a-z\.]{2,6}` which instructs the regex to match 2-6 characters with the `[a-z\.]` criteria.

### Character Classes

* One can distinguish between various character types due to character classes. Our character classes for this regex are located in the "[]" and consist of "a-z" (which looks for characters between `a` and `z`), and `.` (which represents any single character but must be preceded by `/` within a character set to retain its meaning). Character classes typically only match one character out of a large number of characters, but because our expression employs the greedy match quantifier `+`, the regex is forced to match as much of the string as possible.

### Grouping and Capturing

* There is one thing in our expression worth mentioning for this part `()`. Multiple tokens are grouped together and matched to a string using the symbol `()`. If a match occurs, it recalls that match. There are three unique capture groupings in our expression.

    * `([a-z0-9_\.-]+)` this corresponds to the username
    * `([\da-z\.-]+)` which matches the server name.
    * `([a-z\.]{2,6})` which matches the top-level domain.

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
