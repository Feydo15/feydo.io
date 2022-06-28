---
Layout:
Title: "Reducers and rules of Reducers in Redux"
Date: 2022-06-17
Categories:
---

# Introduction

Today i have learned about Reducers and rules of Reducers in Redux 
A reducer, or reducer function, 
is a plain JavaScript function that defines how the current state and an action are used in combination to create the new state.

# body

reducer , or reducer function.

Here’s an example of a reducer function for a todo app:

const initialState = [ 'Print trail map', 'Pack snacks', 'Summit the mountain' ];
 
const todoReducer = (state = initialState, action) => {
  switch (action.type) {
    case 'todos/addTodo': {
      return [ ...state, action.payload];
    }
    case 'todos/removeAll': {
      return [];
    }
    default: {
      return state;
    }
  }
}
There a few things about this reducer that are true for all reducers:

It’s a plain JavaScript function
It defines the application’s next state given a current state and a specific action
It returns a default initial state if no action is provided
It returns the current state if the action is not recognized
There are two intermediate JavaScript syntaxes used here:

We use the equals sign = to supply a default value for the state parameter.
We use the spread operator (...) to copy the current state and any changed values into a new object, 
not the existing state argument. We’ll explain why in the next exercise.


Rules of Reducers

In the previous exercise, we wrote reducers that returned a new copy of the state rather than editing it directly. 
We did this to adhere to the rules of reducers provided by the Redux documentation:

They should only calculate the new state value based on the state and action arguments.

They are not allowed to modify the existing state. Instead, 
they must copy the existing state and make changes to the copied values.

They must not do any asynchronous logic or have other “side effects”.

By asynchronous logic or “side effects”, we mean anything that the function does aside from returning a value, 
e.g. logging to the console, saving a file, setting a timer, making an HTTP request, generating random numbers.

# conclusion

These rules make Redux code predictable and easy to debug: tests run reliably and other developers know what to expect from your code.
we cant really see them in action since we are using them on a vscode that has no redux 
