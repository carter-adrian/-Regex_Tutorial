# Title (replace with your title)

The purpose of this gist is to walk through what a regular expression is and how to use them. Regular Expressions (Regex) can be used when one is trying to match a certain character combination within a string. This is great for pulling out information from a given body of code as well as being used for validation. For example, this tutorial will follow an example code snippet that can be used to match an email. This tutorial will follow the different components of regular expressions. 

## Summary

I will be describing the "Matching an Email" regex, or regular expression, as shown here: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ A matching email regex would be used to validate an email address. For example, if a user is filling out a form online or answering an inquirer prompt in a node.js program, this regex could be used to make sure they enter an email address when asked for one. Essentially, a regex is defining a search pattern.
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

### Anchors

The anchor is what starts and ends the regular expression. 
In the matching email code, 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, 

the anchors are the `^` and the `$`. This code specifically is saying that we are looking for something that starts with 

`^([a-z0-9_\.-]+)` 

we will define what everything inside the parentheses later in this tutorial, but what the anchor means is that if we are to find a match it has follow those initial guidelines. It also has to end with 

`.([a-z\.]{2,6})$`.

So, it must start and end with the given parameters within the code. If it does not, then it is not a match. 

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, `xyz+` then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

`([a-z0-9_\.-]+)` 

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier `+` means that it has to contain at least one of this in order to have a match. 
### Character Classes

`\d` is present in the given matching email code and what it will match a single letter character, a-z, after the `@` sign in the email address. Basically ensuring that a letter is matched after the `@` in the email and not a number or special character. 

### The OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This is a regex for matching a hex code that uses the OR Operator. 
What this will do is it will match where it starts with the `#` and that has to come first followed by one of the following:

`[a-f0-9]{6}` which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers. 

`|` OR Operator

`[a-f0-9]{3}` it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers. 

### Flags

A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

`/regex/` 

Where the slashes denote where the regular expresssion starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:

* g which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
* m which stands for "multiline" which will search line by line rather than searching through a string as a whole. 
* i which stands for "insensitive" will make the 
regular expression case-insensitive, so capitals and lower-case letters will not deture the matching. 

### Character Escapes

The character that follows it is a special character, as shown in the table in the following section. For example, `\b` is an anchor that indicates that a regular expression match should begin on a word boundary, `\t` represents a tab, and `\x020` represents a space.

A character that otherwise would be interpreted as an unescaped language construct should be interpreted literally. For example, a brace (`{`) begins the definition of a quantifier, but a backslash followed by a brace (`\{`) indicates that the regular expression engine should match the brace. Similarly, a single backslash marks the beginning of an escaped language construct, but two backslashes (`\\`) indicate that the regular expression engine should match the backslash.

## Author

Written by Adrian Carter.

Conatct Jeri:

[GitHub](https://github.com/carter-adrian)

[Email](carter.adrian@gmail.com)