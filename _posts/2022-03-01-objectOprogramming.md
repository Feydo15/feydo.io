---
Layout:
Title:	"Object Oriented Programming"
Date:	2022-03-01
Categories:
---
# introduction
Today i have learned about how to "Use Dot Notation to Access the Properties of an Object" and
"Create a Method on an Object" as well as "Make Code More Reusable with the this Keyword"
under the Object Oriented Programming of 
of javascript.

# body

We can use what we call Dot Notation to access the properties of an Object in JavaScript
like this <let bird = {name:"Rodny", numLegs: "2"}; console.log(bird.name)>

in the example above we have used the Dot Notation on the object name "bird" followed by the name 
of the property "name" to access the value of Rodny.

Objects can also have a special type of property called a method and methods
 are properties that are functions. this adds different behavior to an object ,
 now less take our object of bird for example 
 <let bird = {name:"Rodny", numLegs: "2", };>
 <sayName: function() {return "The name of this bird is " + bird.name + ".";}>
<bird.sayName();>
on our example we have added the sayName method, which is a function that returns a sentence
giving the name of the bird.

NB "the method accessed the name property in the return statement using
bird.name".
While this is a valid way to access the object's property, there is a pitfall here. If the variable name changes, any code referencing the original name would need to be updated as well. In a short object definition, it isn't a problem, but if an object has many references to its properties there is a greater chance for error.

A way to avoid these issues is with the this keyword like this:
<let bird = {name:"Rodny", numLegs: "2", };>
 <sayName: function() {return "The name of this bird is " + this.name + ".";}>
<bird.sayName();>

this is a deep topic, and the above example is only one way to use it. In the current context, this refers to the object that the method is associated with: bird. If the object's name is changed to john, it is not necessary to find all the references to bird in the code. It makes the code reusable and easier to read.

# conclusion
this simply means we can give our object functionalities by using methods and combining them with the this keyword or the normal dot notation .i have really enjoyed the challenges and they make
js little bit easier.

.

 
