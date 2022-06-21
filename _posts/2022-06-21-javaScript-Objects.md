---
Layout:
Title: "Real Life Objects, Properties, and Methods"
Date: 2022-06-21
Categories:
---

# Introduction

Today i have learned about Real Life Objects, Properties, and Methods under basic javascript 

# body

well in real life a car in an object and a person is also an object.
a car has properties like weight and color and methods like start and stop :

now less take the code below as  example of an object :

Objects are described as variables as well but they can contain more information (have more values) than the normal 
variables

let car = "Fiat"; // normal car variable 


This code assigns many values (Fiat, 500, white) to a variable named car:

const car = { name : Fiat,
           model : 500,
          weight : 850kg,
           color : white };  // car Object 

The values are written as name:value pairs (name and value separated by a colon) and
It is a common practice to declare objects with the const keyword.
We define (and create) a JavaScript object with an object literal:
Spaces and line breaks are not important. An object definition can span multiple lines:

const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};

The name:values pairs in JavaScript objects are called properties:

Property	Property Value
firstName	John
lastName	Doe
age	        50
eyeColor	blue

Accessing Object Properties
You can access object properties in two ways:

objectName.propertyName
or
objectName["propertyName"]

Object Methods
Objects can also have methods.

Methods are actions that can be performed on objects.

Methods are stored in properties as function definitions.

Property	Property Value
firstName	John
lastName	Doe
age	50
eyeColor	blue
fullName	function() {return this.firstName + " " + this.lastName;}
A method is a function stored as a property.

Example
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

# conclusion
note In JavaScript, the this keyword refers to an object.

Which object depends on how this is being invoked (used or called).

The this keyword refers to different objects depending on how it is used:

In an object method, this refers to the object.
Alone, this refers to the global object.
In a function, this refers to the global object.
In a function, in strict mode, this is undefined.
In an event, this refers to the element that received the event.
Methods like call(), apply(), and bind() can refer this to any object.
