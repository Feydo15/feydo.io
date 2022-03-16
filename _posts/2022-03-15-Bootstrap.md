---
Layout:
Title: 'Bootstrap'
Date: 2022-03-14
Categories:
---

# Introduction

Today i have learned about how to Create a Bootstrap Button and Create a Block Element Bootstrap
Button under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

Since we know that bootstrap is pre-built with css styles well it also has its own styles for button
elements too,which look much better than the plain HTML ones.

now less create a new button element below and give it the btn and btn-default classes,as well as
the text of like :
<button class="btn btn-default">Like</button>

NB:"The button won't appear since we are using a visual studio with no background config of bootstrap"

we already know that bootstrap is also pre-built with classes so it will target our button element
using the classes we used to style our button.

Normally, our button elements with the btn and btn-default classes are only as wide as the text that they contain. For example:
<button class="btn btn-default">Submit</button>
NB:"The button won't appear since we are using a visual studio with no background config of bootstrap"
This button would only be as wide as the word Submit

By making them block elements with the additional class of btn-block, our button will stretch to fill our page's entire horizontal space and any elements following it will flow onto a "new line" below the block. just like this:
<button class="btn btn-default btn-block">Submit</button>
NB:"The button won't appear since we are using a visual studio with no background config of bootstrap"
This button would take up 100% of the available width.

# conclusion

Note that these buttons still need the btn class.
Add Bootstrap's btn-block class to your Bootstrap button so that it can take 100% Of the available
width.
