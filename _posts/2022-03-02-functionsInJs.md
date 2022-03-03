---
Layout:
Title:	"function that returns a string"
Date:	2022-03-02
Categories:
---
# Introduction 

Today i have learned about how to Create a function that returns 'Hello, world', if the name is undefined or empty string,
if the name is defined, then return Hello, name.

# body

When creating a function we start by typing the word function and followed by the name you would like to name your function then we end with the brackets () like this:
<function greet()>.

Then in order to give our function the conditions that it will function on,We start by passing 
parameter into our function (in this case name is our parameter), and open carly braces after
our function like this <function greet(name){   }> 
We then give our function conditions like for loop,if statement and more based on the question we have given in this case we only need the if statement. Our if statement set the condition/s that we 
need and also state the return statement like this
<function great(name) {

    if(name === "" || name === undefined){
        return 'Hello World';
    }else{
        return "Hello, " + name[0].toUpperCase()+ name.substring(1).toLowerCase();
    }
}>

in this case the if statement state that if name which is our parameter is equal to an empty string
or name is equal to undefined then our function should return the string "Hello world" and else it should return "Hello, name" where name will be the argument that is passed into our function
when we call it just like this: 
<great('feyDo');>

but in order for us to check if our results are true or false and also to check if our functions
is working we use console.log on our function when we call it so that it will show the return on 
the console like this: <console.log(great('feyDo'));
>

# conclusion
we are also able to alter the case Categories of our return statement by using the methods
.toUppercase or .toLowerCase in our return statement
