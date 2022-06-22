---
Layout:
Title: " Object Oriented Programming"
Date: 2022-06-17
Categories:
---

# Introduction

Today i have learned about object literal,function in objects and types of values under
 Object Oriented Programming 
# body

Object literal is the normal syntax of an object for example : let x = {value: 10};

objects have two types of values like reference and primitive where  
primitive store values in a variable that are completely independent in other words
primitives are copied by their value.
example of a primitive:

let x = 10;
let y = x;
x = 20;

in the code above x will return 20 but y will return 10,

 Reference type this are objects which are copied by their reference 
 Object are copied by their reference

  let A = {value:10};
 let B = A;
 A.value = 20;

 in the code above  A will return 10 and B will also return 10 because the value of A is stored
 as a reference on the memory that can be accessed by B .


 function or methods in side an object
  function createCircle(radius) {
  // return{
      // radius,
      // draw: function(){
          // console.log("draw")
      // }
  // }; 
 }
 const  circle = createCircle(1);
 circle.draw();


 <Constructor function
function Circle(radius){
 // this.radius = radius;
 // this.draw = function(){
     // console.log("draw")
 // }
} 
// 
Circle.call({}, 1) alt method of calling our function where the first arg specify the object and
 the second specify the properties
const another = new Circle(1);>

# conclusion
please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.