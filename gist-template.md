#  Understanding Matching Url Regex
A Regex (Regular Expression) is a pattern or filter used to validate matches. Regex are literals strings which then get used by searching algorithms to validate inputs.


## Summary

This gist is about the Matching Url Regex 
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```
 This Regex starts with http or https to determine which protocal to search for. It is then followed by escape charcters plus // since / is used to identify the start and end of the literal search strings. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes and Bracket Expressions](#character-classes-and-bracket-expressions)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
There are two anchors in this string one being ^ and the other being $. The ^ is used at the start of the string while the $ is used at the end of the string. Anchors don't actually match anything rather they assert that either the string matching will start or end. 

### Quantifiers
The Matching Url Regex uses the {}, * and ? quantifiers. The * means that it will match 0 or more times while the ? means that will match zero or one time. For this regex it means that its needs to match https at most one time. And it allows to match as many times when it finds patterns that are found with the * quantifier. For the { , } its saying that it can match 2 to 6 times. 


### Character Classes and Bracket Expressions

A character class is defined in by all the characters that are in enclosed within []. The url matching regex uses it three times with [a-z\.]  [\/\w \.-] and [\da-z\.-]. 


### Grouping and Capturing

Grouping is done by () which takes the string enclosed inside the () to search for substrings matching with what is in side. In the url matching string it takes what it has from character classes and builds on that to look for multiple letters. 


### Greedy and Lazy Match

Greedy matching is when the string uses the + operator and it tries to get the longest possible outcome from within the string it is validating. Meanwhile the lazy match is when using the ? operator which only tries to find the shortest string or substring that matches in order to fill the desired outcome. It is possible to use both in a literal string by using them inside groupings causing the match to only match a substring. 


## Author

This gist was written by [christian cebrero](https://github.com/cebrero11) 
