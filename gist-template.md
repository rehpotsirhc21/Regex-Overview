# Regex tutorial Email Validation

The intent of this project is to break down the different components of a Regex.

## Summary

Regex stands for regular expression and may also be called a rational expression(per wiki https://en.wikipedia.org/wiki/Regular_expression). A Regex consists of a sequence of characters. These characters are used as a search pattern for text. 

A regular expression can contain several components. For the purpose of this assignment i will be using the following regex: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)


## Regex Components

### Anchors
The anchors indicate the start and the end of the regex. The start is indicated by the ^ and the end is inidcated by the $. The email regex includes both values. They are located right after the first forward slash and before the last forward slash.

### Quantifiers
The qualifiers specify how may instances must be present for a match to be found (https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions). in the regex for email we have the + being used in additiona to the {2, 6}. The + means match one or more times. This means the characters should occur at least once. For the email we need to have at least 1 character before the @ and at least one character after the @. the {2, 6} will allow between 2 and 6 characters of the proceeding [a-z\.]. 


### Character Classes
The character classes are a way of grouping different characters without enforcing any sort of order. There are a few different chracters used in the email regex. The [] are grouping characters together into a character set. There are 3 distinct places where this happens in the email regex one for each portion of the validation. The hyphen(-) between the characters indicate something can be within a range, rather than looking for a single instance of a listed character. In addition to the [] this regex also includes /d which allows a single digit- 1 would pass validation but 11 would fail since there is more than one digit.

The period(.) indcates to match any character.


### Grouping and Capturing
The grouping and capturing classes group characters together. You can see this in the email regex with the () around the different parts of the email validation.
### Bracket Expressions
A bracket expression is a list of characters enclosed in brackets. There are 3 areas where this happens in the email regex. Each character is validated against the list or range within the brackets. in this situation we are looking for alpha between a and z and numeric characters between 0 and 9.
### Greedy and Lazy Match
The email regex includes greedy matches. A greedy match is indicated by the + in the expression. This can be used many times as necessary to make sure characters meet the validation. 
### Boundaries



## Author

This document was authored by Chris. I am a baby web developer and my github can be found at:https://github.com/rehpotsirhc21/Regex-Overview