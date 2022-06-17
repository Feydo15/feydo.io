---
Layout:
Title: " given a string numbers and letters calculate total"
Date: 2022-06-17
Categories:
---

# Introduction

Today i have learned about how to separate numbers from letters if given a string of both then culculate the total using methods of working 
with arrays

# body

if we are given a string of numbers and letters like this: let string = '4T354B3434234234234'
we first need to create a function that will help us achive our goal since we are working with a string we need to split it so that we can use other methods of arrays on it like filter and reduce,
now we need to use the filter method to filter out the letters from the numbers using the parseInt  
to help us separate them, there fore we use the reduce method hand in hand with the .parseInt
to culculate the total sum of the numbers in the string.

now less take this code for example :

// given a string numbers and letters calculate total


let string = '4T354B3434234234234'

getTotalString = (string) =>{

let newString = string.split("");
let numbers = newString.filter(v => parseInt(v)).reduce((a, b) => parseInt(a) + parseInt(b));

console.log("numbers",numbers);
}

getTotalString(string);


note that the function will work with any argument that we pass to it in other  words the function 
can be used over and over again provided we have another string to use.

# conclusion

please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.