---
Layout:
Title: 'Functional Programing'
Date: 2022-03-08
Categories:
---

# Introduction

Today i have learned that a common pattern while working with arrays is when you want to remove 
items and keep the rest of the array. i have learned about how
Remove Elements from an Array Using slice Instead of splice 
under Functional Programming on the JavaScript 
Algorithms and Data Structures.


# body

The splice method takes arguments for the index of where to start removing items, then the 
number of items to remove and If the second argument is not provided, the default is to 
remove items through the end. However, the splice method mutates the original array it is called on,
just like this:

<const animals = ["Cat","Cow","Chicken","Duck","Bird", "Dog"]
animals.spice(2, 1);>

In this case the splice returns the sting "chicken" and deletes it from the animals
array. animals will have the value ["Cat","Cow","Duck","Bird","Dog"].

The slice method does not mutate the original array , but returns a new one which can be saved into 
a variable.
The slice method takes two arguments for the indices to begin and end the 
slice (the end is non-inclusive), and returns those items in a new array. 
Well using the slice method instead of splice helps to avoid any array-mutating side effects.


# conclusion

using slice instead of splice help mostly where we don't want to mutate over the original
array but return a new one that can also be stored in a variables
splice method is more easier to use.
