---
Layout:
Title:	"Basic Data Structures"
Date:	2022-02-25
Categories:
---
# introduction

Today i have learned about how to "Add Items to an Array with push() and unshift()" 
under the basic data structures of 
js which is mostly applied when working with Array  

# body

The Array`s length, the data types it contain, is not fixed.The Arrays are mutable meaning that arrays can be defined with a length of any number of elements, and elements can be added or removed
over time. Array.push() and Array.unshift() are some of the methods with which we can programmatically modify an array.

both methods take one or more elements as a parameter and add those elements to the array the method 
is being called on. The push() method adds elements to the end of an array , and Unshift() add elements to the beginning like this 
<let  num = 7
let numbers = [4,5,6]>

<numbers=push(num)>

Now  numbers array will have this values [4,5,6,7]

and if we use the unshift() method like this

<numbers.unshift(1,2,3)>

then our numbers array will have this values [1,2,3,4,5,6,7]


# conclusion

this methods help us to mutate through an array and we can add some values to an existing array
like i have illustrated above. 
i still need more examples so that i will get deeper and understand them better.
