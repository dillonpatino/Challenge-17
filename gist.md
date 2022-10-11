# Matching an Email: Regular Expression Tutorial

Regular Expression or Regex, is a sequence of characters that define a search pattern, the same way you use CTRL + F to word search any word in a document.  With Regex, you can use it to find anything not just words. You can define your pattern to search for "literal" characters, which are exactly what they mean.  An "I" is literally an "I" and when searched for with Regex, it will find all text that have the letter "I" in it. You can also use "meta" characters to either be more specific or search for types of characters. You can use a code like `\d\d\d` and it will find any 3 digits that are in groups of three, as opposed to literal characters like `999` which will only find exactly "999". 

## Summary

This Regex tutorial will be focusing on the expression of matching an Email with code that looks like this `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. Using a combination of literal and meta characters, you can make a code that searchs for patterns in emails to ensure that they meet the minimum criteria. Instead of matching email for one that matches exactly "test@gmail.com", you can using Regex to find any and all emails using code similar to the one given above.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)

## Regex Components
-Literal Characters: Characters that are literally the characters in the text(explained in intro) and wrapped in slash characters `/`. 

-Meta Characters: Characters that are a mix of special characters `\` `*` `.` and others with text to make a sequence that is able to give variety instead of matching exactly to the literal characters.


### Anchors
There are two anchors used in the Regex above:
    `^` is used when indicating the beginning of a string.
    `$` is used when indicating the ending of a string.


### Quantifiers
This email Regex uses two quantifiers:
    `+` is an operator that allows us to connect a users email name + the email service + the `.com`.
    `{}` a quantifier that will allow a match range `{2,6}` for a character set of `[a-z\.]`.


### Character Classes
This email Regex uses one character class:
    `\d` matches a singular character that is a digit 0-9.


### Grouping Constructs
As all email addresses include a user's email name, email service, and a `.com`, `.org`, etc...
This Regex has three grouping constructs for each of them:
    `([a-z0-9_\.-]+)` is the first group that matches the user email name. 
    `([\da-z\.-]+)` is the second group that matches the email service.
    `([a-z\.]{2,6})` is the third group that matches the `.com`.


### Bracket Expressions
This email Regex uses 3 bracket expressions for email validation:
    `[a-z0-9_\.-]` matches any case sensitive letter a-z and a character 0-9 and can include a `_`, `.`  or `-`.
    `[\da-z\.-]` matches a singular digit from 0-9, any case sensitive character a-z and `.`, `-`.
    `[a-z\.]` matches any case sensitive character a-z and a `.`.

## Author

https://github.com/dillonpatino
