Matching an Email

This gist will explain how a regular expression can be used to match an email from a given body of code and what the characters in the string mean.

## Summary

I will be reviewing the following code and explaining what each character stands for and what it will look like in the code.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Back-references](#back-references)

## Regex Components

### Anchors
The ^ and $ are known as achors because they start and finish a string. The ^ starts the string and the $ ends the string.

/**^**([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})**$**/

So, this code in particular is looking for something that starts with **^([a-z0-9_\.-]+)** and ends with **([a-z\.]{2,6})$**.

If the email code does not start and end with the bove anchors, then it is not match.

### Quantifiers
This emial code uses several quantifiers: +, {2,6}, [a-z0-9_-].
The + matches the pattern one or more times. The {2,6} matches the pattern from a minimum of 2 times to a maximum of 6 times. 
The expression ([a-z0-9_-]) will match any string that includes any combination of lowercase letters between a and z and any number between 0 and 9 and the special characters of undescore and/or hyphen.

### Character Classes
The \d in the email code means that it willmatch a single letter character, a-z, after the @ sign in the email address.

### Grouping and Capturing
The email code has three groups: ([a-z0-9_\.-]+), ([\da-z\.-]+), and ([a-z\.]{2,6}). 

The first group must match before moving on to group 2 and group 2 must match before moving on to group 3. 

### Bracket Expressions
The expression in group 1, [a-z0-9_\.-] has to contain letters a-z, numbers 0-9, undescore, hyphen, and a period. 

## Author

This tutorial was created by Antonio Casana.

https://github.com/casanaa 
