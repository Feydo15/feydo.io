---
Layout:
Title: "Immutable Updates and Pure Functions"
Date: 2022-07-05
Categories:
---

# Introduction
today i have learned about Immutable Updates and Pure Functions in 
redux.
In programming, there is a more general way to describe the three rules of reducers in Redux: reducers must make immutable updates and be pure functions.

# body
If a function makes immutable updates to its arguments, it does not change the argument but instead makes a copy and changes that copy. 
(Sounds similar to rule 2, no?) It’s called updating immutably because the function doesn’t change, or mutate, the arguments.

This function mutates its argument:

const mutableUpdater = (obj) => {
  obj.completed = !obj.completed;
  return obj;
}
 
const task = { text: 'do dishes', completed: false };
const updatedTask = mutableUpdater(task);
console.log(updatedTask); 
// Prints { text: 'do dishes', completed: true };
 
console.log(task); 
// Prints { text: 'do dishes', completed: true };
Meanwhile, this function “immutably updates” its argument:

const immutableUpdater = (obj) => {
  return {
    ...obj,
    completed: !obj.completed
  }
}
 
const task = { text: 'iron clothes', completed: false };
const updatedTask = immutableUpdater(task);
console.log(updatedTask); 
// Prints { text: 'iron clothes', completed: true };
 
console.log(task); 
// Prints { text: 'iron clothes', completed: false };
By copying the contents of the argument obj into a new object ({...obj}) and updating the completed property of the copy, 
the argument obj will remain unchanged.

Note that, plain strings, numbers, and booleans are immutable in JavaScript so we can just return them without making a copy:

const immutator = (num) => num + 1;
const x = 5;
const updatedX = immutator(x);
 
console.log(x, updatedX); // Prints 5, 6
If a function is pure, then it will always have the same outputs given the same inputs.

This is a combination of rules 1 and 3:

Reducers should only calculate the new state value based on the state and action arguments.
Reducers must not do any asynchronous logic or other “side effects”.
In this example, 
the function is not a pure function because its returned value depends on the status of a remote endpoint.

const addItemToList = (list) => {
  let item;
  fetch('https://anything.com/endpoint')
    .then(response => {
      if (!response.ok) {
        item = {};
      }
 
      item = response.json();
   });
 
   return [...list, item];  
};
The function can be made pure by pulling the fetch() statement outside of the function.

let item;
  fetch('https://anything.com/endpoint')
    .then(response => {
      if (!response.ok) {
        item = {};
      }
 
      item = response.json();
   });
 
const addItemToList = (list, item) => {
    return [...list, item];
};

# conclusion
note that immutable functions does not change the argument but instead makes a copy and changes that copy and
mutable makes changes to the argument.