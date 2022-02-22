---
Layout:
Title:	"Regular Expressions"
Date:	2022-02-21
Categories:
---


# introduction
 
Today i have learned about how specify the exact number of matches, check for all or none, 
positive and negative lookahead as well as check for mixed grouping of characters


# body

To specify the exact number of matches we need to have just one number between the curly brackets on 
 my regex like this /ha{5}h/ in this way it will match only the word hah with the letter a  5 times

 We can also specify the possible existence of an element with the question mark ? .it will check for
 zeros or one of the preceding element.

 Positive lookahead looks to make sure the element in the search pattern is there, but won`t actually
 match it. Positive lookahead is used as (?=...) where the ... is the required part that is not matched and the negative lookahead is used as (?!...) where ... is the pattern you do not want to be there.

 You can also check for mixed grouping of characters in this way /P(engu|umpk)in/

 # conclusion

 i still need more time using different examples of the regular Expression so that i can understand
 better