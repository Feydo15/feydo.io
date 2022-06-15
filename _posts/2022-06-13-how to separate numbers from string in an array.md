---
Layout:
Title: "How to separate numbers from string and push it in a new array"
Date: 2022-06-13
Categories:
---

# Introduction

Today i have learned about how to separate numbers from string and push it in a new array using methods of working with arrays

# body

for better understanding less first declare 2 empty arrays names as numbers and strings
note that naming our variables or arrays should be meaningful;

then use the for each method to access the array there after we use the if statement with
the type of method to separate the numbers from strings , this will help us to push the correct values
into the correct array and join them together in their correct order using concat method like this:
output["A","B","C","M",1,2,3,4,5,6].

now less take this code below for example:

<var array = [1,2,3,"A","B","C",4,5,6,"M"]

let numbers = [];
let strings = [];

array.forEach(element => {
if(typeof(element) === "string"){
string.push(element)
}else if(typeof(element) ==== "number"){
numbers.push(element)
}
})

let output = strings.concat(numbers)
>


# conclusion

please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.