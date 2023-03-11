# How to Use an Email Matching Regular Expression

In this tutorial, you will learn how to read and use the regular expression (regex) shown below. This regex's purpose is to search data for an email address.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z]{2,6})$/

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

The last anchor used is the dollar sign ($). It matches right after the last character in the string. Because code moves through expressions from left to right, for a string to match entirely it must match each component or it will not appear as a match. This means that only those strings that have matched all of the prior expressions will make it to this very last one. In this case, even if it matches all other components, it will not be matched if the last character is not in the pattern collection. Therefore, it must end with a letter (a through z) and be matched at least twice, but no more than six times. (This allows for email addresses that end in only two character such as .us, .ca, etc. (country specific email addresses) or that end in longer strings such as .info, .coop, .museum, etc.).

### Quantifiers
The two quantifier used in this regex are the plus sign (+) and min/max expression of {N, M}. 

The plus sign means that to be truthy, the string must match at least one or more characters in the pattern collection. There isn't a limit to how many matches can be made. This quantifier applies to the string to the left of the at symbol (@) and to the first string to the right of the at symbol (anything between @ and dot (.)).

The second quantifier is the min/max expression {N, M}, where N is the minimum times (characters) the string must match and M is the maximum times it can match. We want to make sure that all valid domain names can be used. See above example in the [Anchors](#anchors) section for examples of short and long domain names.

### OR Operator

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z]{2,6})$/

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
