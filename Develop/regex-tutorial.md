# How to Use an Email Matching Regular Expression

In this tutorial, you will learn how to read and use the regular expression (regex) shown below. This regex's purpose is to search data for an email address.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Being able to do so can be very useful in business settings as it allows a program to verify if the user has entered a valid email address or to find email addresses stored within data strings. Those aren't the only two applications of this regex - as you read on, you may think of your own useful purposes for it!

## Summary

The regex we'll be looking at will be used to find emails matching

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
The first anchor used in this regex is the caret (^). It matches the position before the first character in the string to the pattern collections shown. In this case, it will match any character that is alphabetical (a through z), numerical (0 through 9), or an underscore (_). Any string that does not begin one of those ways, will not be matched.   

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z]{2,6})$/

The last anchor used is the dollar sign ($). It matches right after the last character in the string. Because regex move through the expression from left to right, for a string to match entirely it must match each component or it will not appear as a match. This means that only those strings that have matched all of the prior expressions will make it to this very last one. In this case, even if it matches all other components, it will not be matched if the last character is not in the pattern collection. Therefore, it must end with a letter (a through z) and be matched at least twice, but no more than 6 times. (This allows for email addresses that end in only 2 character such as .us, .ca, etc. (country specific email addresses) or that end in longer strings such as .info, .coop, .museum, etc.).

### Quantifiers
To eliminate anything that is not an email, we can use a quantifier to only find strings that contain one @ symbol. Therefore, we will use @{1} in the regex. 

Because an email address can be many characters long, the quantifier we use will need to allow for many repeats. I'm going to use {N,}, where N is 1 and the number of times it searches is (basically) unlimited.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

/\w+$/ to search for ".com" or ".edu" at the end of an email address

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
