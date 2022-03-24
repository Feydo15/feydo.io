---
Layout:
Title: 'Bootstrap'
Date: 2022-03-23
Categories:
---

# Introduction

Today i have learned about how to Add Font Awesome Icons to our Buttons under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

Well Font Awesome is a convenient library of icons. These icons can be webfonts or vector graphics. These icons are treated just like fonts. You can specify their size using pixels, and they will assume the font size of their parent HTML elements. We can include Font Awesome in any app by adding the following code to the top of your HTML:

<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css" integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf" crossorigin="anonymous">

The i element was originally used to make other elements italic, but is now commonly used for icons. we can add the Font Awesome classes to the i element to turn it into an icon, for example:
<i class="fas fa-info-circle"></i>

Note that the span element is also acceptable for use with icons just like this:
<span class="fas fa-info-circle"></span>

if we were to use Font Awesome to add a thumbs-up icon to our like button by giving it an i element with the classes fas and fa-thumbs-up and also make sure to keep the text Like next to the icon
it would be like This:

<button class="btn btn-block btn-primary"><i class="fas fa-thumbs-up"></i>Like</button>
NB:"The button won't appear since we are using a visual studio with no background config of bootstrap"

# conclusion

bootstrap really helps us to style our apps easier,better and faster
