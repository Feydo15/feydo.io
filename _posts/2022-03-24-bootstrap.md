---
Layout:
Title: 'Bootstrap'
Date: 2022-03-24
Categories:
---

# Introduction

Today i have learned about how to Responsively Style Radio Buttons and Responsively Style Checkboxes under the Front End Development Libraries.
Well Remember Bootstrap is a front end framework used to design responsive web pages and applications. It takes a mobile-first approach to web development, and includes pre-built CSS styles and classes, plus some JavaScript functionality.

# body

We can use Bootstrap's col-xs-* classes on form elements, too! This way, our radio buttons will be evenly spread out across the page, regardless of how wide the screen resolution is.

now less nest 2 radio buttons within a <div class="row"> element. Then nest each of them within a <div class="col-xs-6"> element.

Note: As a reminder, radio buttons are input elements of type radio.
<div class="row">
<div class="col-xs-6">
    <label><input type="radio" name="indoor-outdoor"> Indoor</label>
    </div>
    <div class="col-xs-6">
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
     </div>
 </div>
 note: since we are using a visual studio with no background config of bootstrap we cant really see the
 radio buttons and the effect of bootstrap on them.


 Since Bootstrap's col-xs-* classes are applicable to all form elements, we can use them on our checkboxes too! This way, the checkboxes will be evenly spread out across the page, regardless of how wide the screen resolution is.

now less nest all 2 checkboxes in a <div class="row"> element. Then nest each of them in a <div class="col-xs-4"> element.
Note: As a reminder, checkboxes are input elements of type checkbox.
<div class="row">
<div class="col-xs-4">
<label><input type="checkbox" name="personality"> Loving</label>
</div>
<div class="col-xs-4">
<label><input type="checkbox" name="personality"> Lazy</label>
</div>
 </div>
 note: since we are using a visual studio with no background config of bootstrap we cant really see the
 checkboxes and the effect of bootstrap on them.

 # conclusion
 bootstrap makes styling easier and it helps with the responsiveness of out elements which we had to 
 do them manually on css.