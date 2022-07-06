---
Layout:
Title: "Dispatch Actions to the Store"
Date: 2022-07-04
Categories:
---

# Introduction
today i have learned about how to Dispatch Actions to the Store in 
redux.
The store object returned by createStore() provides a number of useful methods for interacting with 
its state as well as the reducer function it was created with.
# body

The most commonly used method, store.dispatch(), can be used to dispatch an action to the store, 
indicating that you wish to update the state. Its only argument is an action object, 
which must have a type property describing the desired state change.

const action = { type: 'actionDescriptor' }; 
store.dispatch(action);
Each time store.dispatch() is called with an action object, 
the store’s reducer function will be executed with the same action object. 
Assuming that the action.type is recognized by the reducer, the state will be updated and returned.

Let’s see how this works in the lightswitch application from the last exercise:

import { createStore } from 'redux';
 
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
 
console.log(store.getState()); // Prints 'on'
 
store.dispatch({ type: 'toggle' }); 
console.log(store.getState()); // Prints 'off'
 
store.dispatch({ type: 'toggle' });
console.log(store.getState()); // Prints 'on'
In this example, you can also see another store method, store.getState(), 
which returns the current value of the store’s state. 
Printing its value between each dispatched action allows us to see how the store’s state changes.

# CONCLUSION

Internally, when the store executes its reducer, it uses store.getState() as the state argument. 
Though you won’t see it, you can imagine that, when an action is dispatched like this…
store.dispatch({ type: 'toggle'});
…the store calls the reducer like this:
lightSwitchReducer(store.getState(), { type: 'toggle' });
