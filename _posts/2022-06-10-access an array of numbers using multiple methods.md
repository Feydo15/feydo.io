---
Layout:
Title: " access an array of numbers using multiple methods"
Date: 2022-06-09
Categories:
---

# Introduction

Today i have learned about how to access an array of numbers using multiple methods of working with arrays

# body
 So given an array of numbers (ages) i had to check if the ages are greater or equal to 21 .

const ages = [33, 12, 20, 16, 5, 54, 21, 44, 61, 13, 15, 45, 25, 64, 32]; 

first we have to create an empty array tha will hold all the ages that are >= 2,

let canDrink = [];

then we do a for loop with the if statement that  will return and push all the ages that are
>= 2 into our empty array we created earlier just like this: 

for(let i = 0; i < ages.length; i++){
  if(ages[i] >= 21)
  canDrink.push(ages[i])
}
 
 on this line we use several methods of working with arrays to 
 map: use the map() method to map all the ages and multiply them by 2,
 filter: use the filter() method to filter all ages that are >= 40,
 sort: use the sort() method to sort all the ages in an descending order and then,
 reduce: use the reduce() method to add all the ages up and get their sum just like i did below:


const combinedArray = canDrink
  .map((age) => age * 2)
  .filter((age) => age >= 40)
  .sort((a, b) => a - b)
  .reduce((a, b) => a + b, 0);
console.log(combinedArray);

# conclusion

please note that you will need to copy and run this function on a .js file or on a browser
console in oder to see the results and functionality of this function.