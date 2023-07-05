# Boyd's Regex Tutorial

JavaScript is in a programming language of it's own and has really developed over time. With a variety of methods that can be used, like verifying if a string encompasses particular phrases, letters, special characters, etc.

Methods can either be more on the limited spectrum of direct matches. This tutorial will represent the dynamic capabilities with regular expressions, which are a series of of special chatracters that define a search pattern. We will look at email as the particular regex component of this tutorial.

## Summary

The regex expression example we will be reviewing is matching an email expression. We will describe components like  anchors and quantifiers, grouping constructs, bracket expressions, character classes, and character escapes.

The code snippet for matching an email expression is:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. When using applications/technologies like Node or MongoDB.

With this we can find certain patterns in a string and replace find characters in string input.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

In this regex expression (`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. ), particular anchors like ^ are used to represent the beginning of a string and the $ is symbolic for the end of the string. Essentially, these match a position before or after characters in a string.

### Quantifiers

The + operator is the bridge to the user email name  + email service + .com. For example, in the email "boydstacken@icloud.com," the '+' operator is the bridge connecting the username "boydstacken" with the email server "icloud" and the domain type ".com"

The + connects all of these elements of an email together as a string.

 One of the main quantifiers in this regex is the {2,6} which allows a match range of 2-6 characters for the character range of [a-z\.] For example, an email with the name "fred" would cue correctly but "freddie" would not as it exceeds the limit of 6 characters.

### Grouping Constructs

Grouping constructs allow us to break up sections so we can verify if various parts of a string actually fulfill different requirements. They are classified by using parantheses () in a regex expression. 

First group construct here is ([a-z0-9_\.-]+) which is the username of an email i.e. "boydstacken" in the email boydstacken@icloud.com. The second construct is ([\da-z\.-]+) which is the email service (the email service "icloud" form the particular example above).The third is ([a-z\.]{2,6}) which is the domain portion of the email address (.com).


### Bracket Expressions

Bracket expression resemble a desired range of characters we want to match/include.

[a-z0-9_\.-], this means we want to look for lowercase letter between a -z, digits 0-9, _ matches an underscore character and \. matches a period/dot characters\. Everything here matches lowercase letters, digits, or a period character. 

### Character Classes

Character classes specify a range or set of characters valid within a particular area of a pattern and are usually enclosed with `[]`. With the email regex expression there a few character classes used.  This character class[a-z0-9_\.-] matches lowercase letter from a-z, digits 0-9, underscore, period or a hyphen. Secondly, the [\da-z\.-] class represents a single character any lowercase letter from a-z, digits from 0-9, a period/hyphen character. Finally, the [a-z\.] is the third character class matching a single character with a lowercase latter from a-z or a period character.

For example, the email boydstacken@icloud.com, boydstacken (username) is the first class, followed by icloud (the email source) and then the last class .com (domain type).


### Character Escapes

Character escapes are used to match specific characters with specialized meaning. In the matching an email regex expression, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` character escapes are representated with backslashes "\" and followed by a special character. The notable one in all groups is the "\." which matches a period in each parts of the email address. This allows the first portion (username) of an email to contain periods (boyd.stacken instead of just boydstacken), and the third area to enable the "." with the ".com" part of the domain with the period. The other character escape is the "\d" which is used in the scond group to match a digit (0-9) in the email service part of the email ("icloud245" instead of "icloud").

## Author

Boyd Stacken
https://github.com/boydstacken
boydstacken@icloud.com