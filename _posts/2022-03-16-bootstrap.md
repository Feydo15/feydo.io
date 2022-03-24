---
Layout:
Title: 'Bootstrap'
Date: 2022-03-16
Categories:
---

# Introduction

Today i have learned about how to Taste the Bootstrap Button Color Rainbow and Call out Optional Actions with btn-info under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

The btn-primary class is the main color we will use in our app. It is useful for highlighting
actions we want our user to take.
all we need to do is to replace bootstrap's btn-default class with btn-primary in our button
and is some cases we can just use both of them on one button.
we must not forget that this button will still need the btn and btn-block classes.
less take this code for example :<<button class="btn btn-default btn-block">Delete</button>>
now to add our main color to our button all we need to do is to replace btn-default class with
btn-primary but still keep our btn and btn-block classes like this:
<<button class="btn btn-primary btn-block">Like</button>>

Well bootstrap comes with several pre-defined colors for buttons. The btn-info class is used to
call attention to optional actions that the user can take.
Now less create a block-level bootstrap button with the text Info, and add bootstrap`s btn-info
class to it.
we also must not forget that this button will still need the btn and btn-block classes.
well less take this code for example:<<button class="btn btn-block btn-info">Info</button>>
in both cases our buttons still have the btn and btn-block classes and the only difference is
the text of the button, the classes of btn-info and btn-primary.

# conclusion

well bootstrap makes styling our app easier because it is pre-defined well i still need more
examples so that i can get used to the way bootstrap work or function.
note that we cant really see the buttons we created since we are using a visual studio with no background config of bootstrap.
