---
Layout:
Title: "create a function that use multiple methods"
Date: 2022-06-09
Categories:
---

# Introduction

Today i have learned about how to create a function that use multiple methods 
working with arrays

# body

the function is supposed to 
1 combine and sort 2 arrays
2 filter all the even and odd numbers and push each into their individual new arrays

3 find the sum of the even numbers and also the sum of the odd numbers then add the 2 to get the total 

now less take the code below for example:

<let Array1 = [5,7,9,2,6];
let Array2 = [1,4,8,0,3];


const combinedSortedArray = (a , b) =>{
let newArray = a.concat(b).sort((a , b) => b - a)
let oddNum = newArray.filter((a) => a % 2)
let evenNum = newArray.filter((a) => a % 2 == 0)

let tot = oddNum.reduce((a, b) => a + b)
let tots = evenNum.reduce((a, b) => a + b);

let sumTot = tots + tot;

console.log('tot', sumTot)
}

combinedSortedArray(Array1 , Array2)

>

this function uses the concat(),filter(),reduce() and sort() methods

# conclusion
please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.