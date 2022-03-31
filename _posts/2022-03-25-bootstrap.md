---
Layout:
Title: 'Bootstrap'
Date: 2022-03-25
Categories:
---

# Introduction

Today i have learned about how to Style Text Inputs as Form Controls
and Line up Form Elements Responsively with Bootstrap under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

We can add the fa-paper-plane Font Awesome icon by adding <i class="fa fa-paper-plane"></i> within our submit button element.

Less give our form's text input field a class of form-control.give our form's submit button the classes btn btn-primary. Also give this button the Font Awesome icon of fa-paper-plane.

All textual <input>, <textarea>, and <select> elements with the class .form-control have a width of 100%.

<input type="text" class="form-control"placeholder="input text" required>
<button type="submit" class="btn btn-primary"><i class="fa fa-paper-plane">Submit</button>

Now let's get our form input and our submission button on the same line. We'll do this the same way we have previously: by using a div element with the class row, and other div elements within it using the col-xs-\* class.

less nest both our form's text input and submit button within a div with the class row. Nest our form's text input within a div with the class of col-xs-7. Nest our form's submit button in a div with the class col-xs-5.

<div class="row">
<div class="col-xs-7">
<input type="text" class="form-control"placeholder="input text" required>
</div>
<div class="col-xs-5">
<button type="submit" class="btn btn-primary"><i class="fa fa-paper-plane">Submit</button>
</div>
</div>

# conclusion

with more examples and more practice i will understand it better and be used to using bootstrap
as it makes styling our apps easier.
