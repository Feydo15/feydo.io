---
Layout:
Title: 'Bootstrap'
Date: 2022-03-22
Categories:
---

# Introduction

Today i have learned about how to Use a span to Target Inline Elements and Create a Custom Heading under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

We can use spans to create inline elements. Remember when we used the btn-block class to make the button fill the entire row?
That illustrates the difference between an "inline" element and a "block" element.
By using the inline span element, we can put several elements on the same line, and even style different parts of the same line differently.
Using a span element,less nest the word love inside the p element that currently has the text "Things dogs love". Then give the span the class text-danger to make the text red:
<<p>Things dogs <span class="text-danger">love:</span></p>>

We will make a simple heading for our App by putting the title and image in the same row.
Remember, Bootstrap uses a responsive grid system, which makes it easy to put elements into rows and specify each element's relative width. Most of Bootstrap's classes can be applied to a div element.

less nest our image and our h2 element within a single <div class="row"> element.nest our h2 element within a <div class="col-xs-8"> and our image in a <div class="col-xs-4"> so that they are on the same line. This will make our image to be the right size to fit along the text.
less take this code for example :
<<div class="row">

<div class="col-xs-8">
 <h2 class="text-primary text-center">exampleApp</h2>
</div>
<div class="col-xs-4">
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" class="img-responsive" alt="Three kittens running towards the camera.">
</div>
</div>>
note that we cant really see the image we created since we are using a visual studio with no background config of bootstrap.

# conclusion

bootstrap makes styling easier but we still need to use css some how on our apps
