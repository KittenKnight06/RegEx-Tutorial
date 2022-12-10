# ReGex Tutorial

RegEx is a tool that may be used to define a search term parameter, and can be applied in many differnt circumstances, accross multiple coding languages.

## Summary

In this tutorial, the following code is used for matching emails, we can use this code to validate that an email follows the correct format/pattern.

Matching Email:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

* ### Anchors

The anchor is what starts and ends the regular expression. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In this matching email code, the anchors are the ^ and the $. This code specifically is saying that we are looking for something that starts with 

`^([a-z0-9_\.-]+)`

and it has to end with

`.([a-z\.]{2,6})$.`

It must start and end with the given parameters within the code. If it does not, then it is not a match.

* ### Quantifiers

Quantifiers indicate that the preceding token must be matched a certain number of times. If we look at our code for matching the email:

`([a-z0-9_\.-]+)` will match any string that contains `a-z`, `0-9`, `_`, `.`, or `-`, the quantifier `+` means that it has to contain at least one of this in order to have a match. 

`{2,6}` would retrun a positive match for items containing between 2 and 6 characters

* ### Grouping Constructs

`()` is used to group the code, for example `([a-z0-9_\.-]+)` is the first group that appears in this regex. This must be true before moving on to "match" the next part of the code. `([\da-z\.-]+)` is the second group that appears in this regex, and`([a-z\.]{2,6})` is the third group.

Using the first group `([a-z0-9_\.-]+)` as an example, this regex matches any letter or number a-z or 0 to 9, accepts underscores, periods and dashes. Then the quantifier matches one or more of the previous token.

* ### Bracket Expressions

Bracket expressions are the syntax theroy on combining character classes. Multiple character classes may be combined in a single bracket expression.

For example `[a-z0-9_\.-]` where regex would match any letter, number, an underscore, and a hyphen.

* ### Character Classes

Character classes match a character from a specific set. 

Example of some predefined character classes are listed as below:

a. `[ABC]` Characters inside brakets will match any character in the set.

b. `[A-Z]` Add a dash between two characters will select a Range.

c. `\d` Matches any digit character (0-9).

d. `\p` Matches a character in the specified unicode category.

Looking at the second group of the regex `([\da-z\.-]+)` after the `@`, the rules are the domain name must be matched with can use one or more digits, letters between a-z, periods, and hyphens. The domain name is then followed by a period `\.`.

* ### The OR Operator



* ### Flags

* ### Character Escapes

* ## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
