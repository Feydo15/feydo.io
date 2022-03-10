---
Layout:
Title: 'Functional Programing'
Date: 2022-03-09
Categories:
---

# Introduction

Today i have learned about how to Apply Functional Programming to Convert Strings to URL Slugs
under Functional Programming on the JavaScript
Algorithms and Data Structures.

# body

There are a number of useful array and string methods that follow functional programming principles.
like reduce method<[.reduce()]>, which is a powerful method used to reduce problems to simpler
forms. From computing averages to sorting, any array operation can be
achieved by applying it. Recall that map and filter are special cases of reduce.

Many content management sites (CMS) have the titles of a post added to part of the URL for simple
bookmarking purposes.
For example, if you write a Medium post titled Stop Using Reduce,
it's likely the URL would have some form of the title string in it (.../stop-using-reduce).

less take this example:
<var globalTitle = "Winter Is Coming";// the global variable
function urlSlug(title) {
return title
.toLowerCase()
.trim()
.split(/\s+/)
.join("-");
}>
<var winterComing = urlSlug(globalTitle); // Should be "winter-is-coming">

Well in this case we took our input which is a string with spaces and title-cased words
then returned our output which is a string with the spaces between words replaced by a hyphen (-)
our function also turns our output to all lower-case letters
using <[.toLowerCase()]>

# conclusion

i have learned so much about the split method and also map and filter methods
and slipt and join helps a lot if u can't use the reduce method.
