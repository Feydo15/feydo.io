---
Layout:
Title: "given a list of items return numbers"
Date: 2022-06-14
Categories:
---

# Introduction

Today i have learned about how to given a list of items return numbers using methods of working 
with arrays

# body

if we are given a list of items like this: list = ['5' , 'g' , 3 , 5 , 10 , 'dfdfdf']
which is an array we first need to create a function that will first filter and map the array using
the .filter() and .map() methods and passing our list as an argument to the function and also 
call back our function passing our list as an argument.

now less take this code for example :

// given a list of items return numbers

let phrase =['5' , 'g' , 3 , 5 , 10 , 'dfdfdf']
let phrase2 =[ 'g' , 3 , 5 , 10 , 'dfdfdf']


const returnNumbers = (phrase) => {

let num = phrase.filter(function(element) {
    return !isNaN(element)
})

let numbers = num.map(function(val) {
    return parseFloat(val)
})
console.log("-------------------")
    console.log(numbers)
}

returnNumbers(phrase2)

note that the function will work with any argument that we pass to it in other  words the function 
can be used over and over again.

# conclusion

please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.