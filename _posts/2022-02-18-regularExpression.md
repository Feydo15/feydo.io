---
Layout:
Title:	"Getting started"
Date:	2022-02-18
Categories:
---
# introduction

What i have learned today based on the Regular Expressions.

match all numbers , all non numbers and match whitespace

# body

To match all numbers we have to use the shortcut \d, with a lowercase d. this is equal to the character class
[0-9] which looks for a single character of any number between zero and nine.
we can also search for non-digits using a similar shortcut that uses an uppercase D instead.
the shortcut to look for non-digits characters is \D. this is equal to the character class 
[^0-9], it looks for a single character that is not a number between zero and nine.

you can also search for whitespace using  the \s which is a lowercase s. this pattern not only matches
whitespace, but also carriage return, tab, from feed, and new line characters.
you can think of it as similar to the character class [\r\t\f\n\v].


# conclusion
the Regular Expressions makes working with regexes more easier but they can be confusing when working
together so they need more attention.