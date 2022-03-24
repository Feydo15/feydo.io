---
Layout:
Title: 'Bootstrap'
Date: 2022-03-18
Categories:
---

# Introduction

Today i have learned about how to Warn Your Users of a Dangerous Action with btn-danger and Use the Bootstrap Grid to Put Elements Side By Side under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

Since we know that bootstrap comes with several pre-defined colors for buttons. The btn-danger class is the button color we will use to notify users that the button performs a destructive action, such as deleting something or some information.
now less Create a button with the text Delete and give it the class btn-danger.
well as long as we are using bootstrap our buttons still need the btn and btn-block classes.
well less take this code for example :<<button class="btn btn-block btn-danger">Delete</button>>
note that we cant really see the buttons we created since we are using a visual studio with no background config of bootstrap.

Bootstrap uses a responsive 12-column grid system, which makes it easy to put elements into rows and specify each element's relative width. Most of bootstrap's classes can be applied to a div element.
bootstrap has different column width attributes that it uses depending on how wide the user's screen is. For example, phones have narrow screens, and laptops have wider screens.
less take for example bootstrap's col-md-_ class. Here, md means medium, and _ is a number specifying how many columns wide the element should be. In this case, the column width of an element on a medium-sized screen, such as a laptop, is being specified. now for example less
Put the Like, Info and Delete buttons side-by-side by nesting all three of them within one <div class="row"> element, then each of them within a <div class="col-xs-4"> element like this:
<<div class="row"><div class="col-xs-4"><button class="btn btn-block btn-primary">Like</button></div><div class="col-xs-4"> <button class="btn btn-block btn-info">Info</button></div><div class="col-xs-4"> <button class="btn btn-block btn-danger">Delete</button></div></div>>
note that we cant really see the buttons we created since we are using a visual studio with no background config of bootstrap.

# conclusion

Bootstrap has a specific color for a specific class that is pre-defined with it and
The row class is applied to a div, and the buttons themselves can be nested within it.
