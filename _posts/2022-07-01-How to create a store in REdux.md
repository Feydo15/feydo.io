---
Layout:
Title: "How to create a store in redux"
Date: 2022-07-01
Categories:
---

# Introduction
today i have learned about how to create a store in 
redux.
The store is an object that enforces the one-way data flow model that Redux is built upon. 
# body

Create a Redux Store

As you know, 
every Redux application uses a reducer function that describes which actions can update the state
and how those actions lead to the next state.

For example, suppose you wanted to build an application for a light switch. 
Its reducer might look like this:

const initialState = 'on';
const lightSwitchReducer = (state = initialState, action) => {
  switch (action.type) {
    case 'toggle':
      return state === 'on' ? 'off' : 'on';
    default:
      return state;
  }
}
This reducer handles a single action type 'toggle' and returns the next state of the store: 
'on' if it had been 'off' and vice-versa. If an unrecognized action is received, 
the current state of the store is returned.

The programmer could manually execute the reducer with the current state of the store 
and the desired action to perform like so:

let state = 'on';
state = lightSwitchReducer(state, { type: 'toggle' });
console.log(state); // Prints 'off'
However, this is the main responsibility of the store. 
The store is an object that enforces the one-way data flow model that Redux is built upon. 
It holds the current state inside, receives action dispatches, 
executes the reducer to get the next state, 
and provides access to the current state for the UI to re-render.

Redux exports a valuable helper function for creating this store object called createStore(). 
The createStore() helper function has a single argument, a reducer function.

To create a store with lightSwitchReducer, you could write:

import { createStore } from 'redux'
 
const initialState = 'on';
const lightSwitchReducer = (state = initialState, action) => {
  switch (action.type) {
    case 'toggle':
      return state === 'on' ? 'off' : 'on';
    default:
      return state;
  }
}
 
const store = createStore(lightSwitchReducer);
For the remainder of this lesson, you will be building a simple counter application, 
whose state is a single number, using the Redux library.

# conclusion
please note : Redux exports a valuable helper function for creating this store object called createStore().
The createStore() helper function has a single argument, a reducer function.