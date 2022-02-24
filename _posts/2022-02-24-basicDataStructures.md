---
Layout:
Title:	"Getting started"
Date:	2018-02-06
Categories:
---
# introduction

Today i have learned about how to "Use an Array to Store a Collection of Data" 
and "Access an Array's Contents Using Bracket Notation" under the basic data structures of 
js which are mainly applied when working with Array  

# body

When we  want to store a collection of data using an array we start by declare your array using let or const like this (let myArray = []) where myArray is the name of your array and [] is
your array, for example 

let exampleArray = ["name" , "age" , 5 , "gender",true] on this example name, age, 5, gender are the 
data that is stored in our Array, well this is a one-dimensional array(meaning it has one level) and we can add different types of data in our array like booleans (true);strings("") and numbers(5)
and we can also Access the length of our array by Array.length like this
 <let exampleArray = ["name" , "age" , 5 , "gender",true] console.log(exampleArray.length)>
  and 5 will appear in our console.

  We can also access our array`s content by using the brackets notation this give`s us the ability to not only store data but to be able to retrieve that data on demand.For example, if we want to retrieve the name from ourArray and assign it to a variable, we can do so with the following code:
  <let exampleArray = ["name" , "age" , 5 , "gender",true]>
  <let ourVariable = exampleArray[0];>
  and we can also  accessing the value associated with an index, you can also set an index to a value using the same notation:

<exampleArray[1] = "not age anymore";>
Using bracket notation, we have now reset the item at index 1 from the string age, to not age anymore. Now exampleArray is ["name", "not age anymore",5 , "gender",true].

# conclusion
i still need to check more example that has more than one-dimensional array so i can 
understand deeper on more complex array and apply the same methods on them.
