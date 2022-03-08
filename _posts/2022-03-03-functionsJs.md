---
Layout:
Title:	"number division function"
Date:	2022-03-03
Categories:
---

# Introduction 


 Today i have learned about how to  create a function that 
 checks if the total number Of workers is divisible by groupOne or groupTwo
under javascript

# body

This function has to check if our first parameter is divisible by the second parameter
and the last parameter which will be passed in our function as arguments when we call it and return a boolean, 
in this case our parameters were number,groupOne and groupTwo so if the number is divisible by both groupOne and
groupTow then our function will return true and if not it will return false.
we created a function called isTotalNumberOfWorkersDivisible and passed number,groupOne and groupTwo
as our parameters like this:
<const isTotalNumberOfWorkersDivisible = (number, groupOne, groupTwo)>

there after we opened our carly braces so that we can state our conditions of the function ie
=> { }, on our function we used if statement to set our conditions and our return statement
like this
<if( (number % groupOne === 0) && (number % groupTwo === 0)){
        return true;
    } else { return false;

    }>
On our conditions is state that if number is divisible by groupOne and the remainder is equal to 0, 
((number % groupOne === 0)) and number is divisible by groupTwo and the remainder is equal to 0, 
((number % groupTwo === 0)) then our function should return true or else it should return
false

We then call our function at the end and pass in our arguments, in this example we used the 
console.log() to call our function so that we can see the return statement on the console

well this is the whole function that we created:

<const isTotalNumberOfWorkersDivisible = (number, groupOne, groupTwo) => {

    if( (number % groupOne === 0) && (number % groupTwo === 0)){
        return true;
    } else { return false;

    }

}

console.log(isTotalNumberOfWorkersDivisible(10, 5, 2))
console.log(isTotalNumberOfWorkersDivisible(8, 10, 4))
>

and we first passed 10,5,2 as our arguments and since 10 is divisible by both 5 and 2 this 
will return true.
then we passed 8,10,4 as our arguments and since 8 is only divisible by 4 and not by 10 
our function will return false

# conclusion
this kind of challenges help us to understand the functions better since we are doing them 
practically so and we have to set the conditions by our self.