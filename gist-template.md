# What is Regex?

>On a very basic level, regular expression(regex) is a set of strings the hold a specific pattern. What this does is matches the pattern that you created with a string from an input field. This then will compare the regex against the string to see if it's a valid input(e.g., verifying phone numbers, checking to see if an email is a valid input, or even searching for things).

>You can create your regex to look for whatever you want! This tutorial will go over how to break down regular expressions sand how you can apply it for your needs.

## Summary

>Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

>The regex we'll be deciphering is /(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{6,}/


## Table of Contents

- [What is Regex?](#what-is-regex)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

### Anchors
>This current regex does not have any anchors. 

>See below for some anchor types:
>- __^s__  matches any string that __starts with s__
>- __s$__  matches any string the __ends with s__
>- __^a$__ matches any string that __starts and ends with a__
>-  __add__ matches any string that __has the text add in it__

### Quantifiers
>This regex has one quantifier: __{6,}__.

>The specifies the number of times a preceding character, group, or character class can be matched. The quantifier __{6,}__ specifies that the preceding character __(.)__ must be matched at least 6 times, meaning that the string must have a length of at least 6 characters.

>The list below demonstrates additional quantifiers:
>- __aar*__ matches a string that has __aa followed by  or more r__
>- __aar+__ matches a string that has __aa followed by at least one or more r__
>- __aar?__ matches a string that has __aa followed by zero or one r__
>- __aar{4}__ matches a string that has __aa followed by four r__
>- __aar{4,}__ matches a string that has __aa followed by four or more r__
>- __aar{1, 2}__ matches a string that has __aa followed by one up to two r__
>- __a(bc)*__ matches a string that has __a followed by zero or more copies of the sequence ar__
>-  __a(ar){1, 2}__ matches a string that has __a followed by one up to two copies of the sequence ar__

### Bracket Expressions
>This regex has two bracket expressions: __[a-z]__ and __[A-Z]__.

>The bracket expression matches the range of characters within the brackets. __[a-z]__ will match lowercase and __[A-Z]__ will match capital letters. These bracket expressions are used in conjunction with the positive lookahead assertions __(?=)__ to ensure the string contains at least one lowercase and one uppercase.

>The list below demonstrates additional bracket expressions functionality:
>- __[aar]__ matches a string that has __either an a or aa or ar__ essentially an or for every character
>- __[a-r]__ same as previous
>- __[a-fA-F0-9]__ a string that represents a __single hexadecimal digit, case insensitively__
>- __[0-9]%__ a string that has a character from __0 to 9 before a % sign__
>- __[^a-zA-Z]__ a string that has __not a letter from a to z or from A to Z.__ In this case the ^ is used as __negation of the expression__

### Character Classes
>This regex has two character classes: __\d__ and __.__

>See the list below for the __\d__ and __.__ character classes that are be used along with the two additional options:
>- __\d__ matches a __single character__ that is a __digit__
>- __\w__ matches a __word character__ (alphanumeric character plus underscore)
>- __\s__ matches a __whitespace character__ (includes tabs and line breaks)
>- __.__ matches __any character__ 

### The OR Operator
>This regex does not have an OR operator.

>The list below describes the OR operator: 
>- __a(a|r)__ matches a string that has __a follow by a or r__ (and captures __a or r__)
>- __a[ar]__ same as the previous, but without capturing a or r

### Flags
>The regex provided does not have any flags.

>Flags are at the end of the expression. The list below provides what flags you can use:
>- __g__ (global) does not return after the first match, restarting the subsequent searches from the end of the previous match 
>- __i__ (insensitive) makes the whole expression not case sensitive.
>- __m__ (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string

### Character Escapes
>This regex has one character escape: __\d__

>A character escape is a way to match a special character. In this case, it is searching for a digit (0-9)

## Author

>Aaron Morgan - I am new to the web development game, but I am looking forward to learning and growing into a successful developer. Currently, I am in the DOD aerospace sector but working on transitioning to a new career path.

>GitHub - https://github.com/craymorgana
