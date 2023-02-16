# Regualr Expression Matching Email Format

The intent of this Gist is to describe the different components of a regular expression that is searching/Matching characters in a Text string that looks for validation and returns the content that is in email format

## Summary
We will break apart the Regalr Expression below to explain the different components. This expression Matches string value that is in E-MAIL format
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
Anchors are the specific characters that define the start and end of the string being searched for. The Start character for the search is "^" and the End character is "$"

### Quantifiers
Quantifiers are the specific characters that define how often certain characters in the search can occur. for the specific example of the Email Search the  "+" character defines a match for the characters before the "+" must appear 1 or more times. The "{2,6}" quantifier defines the minimum and maximum itterations to match

### OR Operator
The "|" , "Or" operator allows two or more matches to be acceptable for a RegEx. The Email example does not use the "Or" operator

### Character Classes
Character Classes define the type of character the RegEx is searching/matching. 
- "[a-z]" matches characters between a to z
- "[abc]" matches the three specific letters in order. can be done with just "[ab]" for only two specific characters
- "\w" matches words
- "\W" matches not words
- "." matches for a single character
- "\d" matches digits
- "\D" matches not digits
- "\s" matches white spaces
- "\S" matches not white space
- For the Email Example the [a-z], and "\d" are applied which means matches can have letters from a-z and the 10 digits

### Flags
Flags are additional conditional options for a specific match in a RegEx. Flags were not used in the Email Example. an example a of commonly used Flags is "i" which ignores if a chracters is capitalized or not

### Grouping and Capturing
Grouping is a term used to seperate certain sections of the Regex so that Operator and Quantifiers and other arguments can be applied to specific parts. The groups are seperated/designated by parenthisis. In the email emxample their are 3 groups. ([a-z0-9_\.-]+) is the first. ([\da-z\.-]+) is the second. ([a-z\.]{2,6}) is the third

### Bracket Expressions
Bracket Expression defines everything that can be matched. For the Email Example in the first group the bracket [a-z0-9_\.-] defines that matches can be all the letters, all the digits and the specifics characters underscore, backslash, period, and hyphen

### Greedy and Lazy Match
Greedy is a term that defines the Matches of RegEx. how the matches are look for the specific charcters. Greedy Matches try to match the designated pattern for every position. if no match match move to next position. Lazy Matches trys to repeat search/matches minimal number of times

### Boundaries
There are three positions that quilify as boundries.
- before the first character in the string, if the first character is a word character
- after the last character in the string, if the last charcter is a word chracter
- between two characters in the string, where one is a word and the other is not a word character
NO boundries were used in the Email Example

### Back-references
Defines a previous Grouping and looks for the same match. Not used in the Email Example

### Look-ahead and Look-behind
Look-ahead and Look-behind are "lookaround" are zero-length assertions. Which means they do not return matches but the possibilty of matches. the returned value of these assertions will be "match" or "no match"

## Author
https://github.com/rasvindra

