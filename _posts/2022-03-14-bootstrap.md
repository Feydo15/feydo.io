---
Layout:
Title: 'Bootstrap'
Date: 2022-03-14
Categories:
---

# Introduction

Today i have learned about how to Make Images Mobile Responsive and Center Text with Bootstrap
under the Front End Development Libraries.
Well Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body
when making images mobile responsive using bootstrap we first have to add an image to our app page
with the attribute of its url and It would be great if this image could be exactly the width of our phone's screen.

Fortunately, with Bootstrap, all we need to do is add the img-responsive class to our image
 and the image should perfectly fit the width of our page, like This:

<<a href="#"><img class="img-responsive" src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" alt="image of the three cats"></a>>

NB:"The image won't appear since we are using a visual studio with no background config of bootstrap"

in this case the class of img-responsive will style our image to fit every screen and src is the source
of our image while alt is the text that will appear on the page if your browser did not or could't 
upload the image just to let you know a little description on the image.

We can also style our text using bootstrap in this case we will center our text in the h2 element and  All we need to do is add the class text-center to our  h2 element.since we know that we can add classes
to the same element by separating each of them with a space, well that is exactly what we are going to 
do on our example below:
<h2 class="red-text text-center">your text</h2>

in this case the text that is contained by our h2 element will have a red color and it will also be 
centered.

# conclusion

with more examples and more practice i will understand it better and be used to using bootstrap
as it makes styling our apps easier.