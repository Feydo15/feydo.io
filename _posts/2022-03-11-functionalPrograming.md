---
Layout:
Title: 'Functional Programing'
Date: 2022-03-11
Categories:
---

# Introduction

Today i have learned about Introduction to Currying and Partial Application
under Functional Programming on the JavaScript
Algorithms and Data Structures.

# body

The arity of a function is the number of arguments it requires. Currying a function means
to convert a function of N arity into N functions of arity 1.

In other words, it restructures a function so it takes one argument, then returns another
function that takes the next argument, and so on.
less take this code for example:

<function unCurried(x, y) {
return x + y;
}

<function curried(x) {
return function(y) {
return x + y;
}
}

> <const curried = x => y => x + y

curried(1)(2)>

on this code curried(1)(2) would return 3
This is useful in your program if you can't supply all the arguments to a function at one time.
You can save each function call into a variable, which will hold the returned function reference
that takes the next argument when it's available.
this is how you can use the carried function in the example above:
<const funcForY = curried(1);
console.log(funcForY(2)); // 3>
Similarly, partial application can be described as applying a few arguments to a function at a
time and returning another function that is applied to more arguments just like this:

<function impartial(x, y, z) {
return x + y + z;
}>
<const partialFn = impartial.bind(this, 1, 2);
partialFn(10); // 13>

# Introduction

i have to do more example or problems about this so that i can have a better understanding
on this one because it is not that clear to me as i wish it should.
