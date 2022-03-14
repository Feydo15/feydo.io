---
Layout:
Title: 'Functional Programing'
Date: 2022-03-10
Categories:
---

# Introduction

Today i have learned about how to Use the every Method to Check that Every Element in an Array
Meets a Criteria and Use the some Method to Check that Any Elements in an Array Meet a Criteria
under Functional Programming on the JavaScript
Algorithms and Data Structures.

# body

The every method works with arrays to check if every element passes a particular test and it returns
a Boolean value-true if all the values meet the criteria, false if not.
less take this code for example :
this code would check if every element in the numbers array is less than 15:
<const numbers = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16];>

<numbers.every(function(currentValue) {
return currentValue < 15;
});>

well on this code the every method would return false because 16 is not less than 15.

Well on the other hand we have the some method which works with arrays to check if any element
passes a particular test and it returns a Boolean value-true if any of the values meet the criteria,
false if not.
less take this code for example :
this code would check if any element in the numbers array is less than 15:
<const numbers = [9,10,13,15,16,18,30];>

<numbers.some(function(currentValue) {
return currentValue < 15;
});>

well on this code the every method would return true because 9,10,13 are less than 15.

# conclusion

keep in mind that every method check if all element meet a certain criteria in an Array and
some method check if any element meet a certain criteria in an Array.
