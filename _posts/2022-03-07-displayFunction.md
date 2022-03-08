---
Layout:
Title:	"Display Functions"
Date:	2022-03-07
Categories:
---


# Introduction 
Today i have learned about how to "Create a function that display my input values to my innerHTML" 
using both javascript and HTML.

# body

The display function provides information about the kind of values that are the result of executing a statement or expression. This information is useful for understanding how a program or script works.
In order to create the Display Function we need to have an input type of a button in our HTML and 
with our onclick method and assign it to our function which we will use in our script like This

<<!DOCTYPE html>
<html>
  <head>
    <title>Title of the document</title>
  </head>
  <body>
    <p>There is a hidden message for you. Click to see it.</p>
    <button onclick="myFunction()">Click me!</button>
    <p id="test"></p>
  </body>
</html>
>

we then move to our script, we can add our script to our HTML as an element or link it as a source
from out side
in our script we create our function with the same function name that we have assigned it with in our HTML on our onclick method just like This

<<script>
      function myFunction() {
        document.getElementById("test").innerHTML = "Hello Dear";
      }
    </script>>

    in this case  when we click our button that we created in our HTML our function will take effect
    and since we told it that we want to display our document which has an id of test in this from
    document.getElementById("test") and added where we want it to display our document by .innerHTML
    when we click our button the string Hello Dear will appear as our value in our P tag section
    that has the id of test in our html

    # conclusion
    there are more ways that we can get our document it can be by id , class or name.
    we can also link our outside script like this <script src "/main.js"></script>
     
    
