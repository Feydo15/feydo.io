---
Layout:
Title: "Respond to State Changes"
Date: 2022-07-06
Categories:
---

# Introduction
today i have learned about how to respond to state changes in 
redux.
 in Redux, actions dispatched to the store can be listened for and responded to using the
 store.subscribe() method
# body
In a typical web application, 
user interactions that trigger DOM events ("click", "keydown", etc…) 
can be listened for and responded to using an event listener.

Similarly, in Redux, actions dispatched to the store can be listened for and responded to using the 
store.subscribe() method. This method accepts one argument: a function, often called a listener, 
that is executed in response to changes to the store‘s state.

const reactToChange = () => console.log('change detected!');
store.subscribe(reactToChange);
In this example, each time an action is dispatched to the store, and a change to the state occurs, 
the subscribed listener, reactToChange(), will be executed.

Sometimes it is useful to stop the listener from responding to changes to the store, 
so store.subscribe() returns an unsubscribe function.

We can see this in action in the light switch application:

// lightSwitchReducer(), toggle(), and store omitted...
 
const reactToChange = () => {
  console.log(`The light was switched ${store.getState()}!`);
}
const unsubscribe = store.subscribe(reactToChange);
 
store.dispatch(toggle());
// reactToChange() is called, printing:
// 'The light was switched off!'
 
store.dispatch(toggle());
// reactToChange() is called, printing:
// 'The light was switched on!'
 
unsubscribe(); 
// reactToChange() is now unsubscribed
 
store.dispatch(toggle());
// no print statement!
 
console.log(store.getState()); // Prints 'off'
In this example, the listener function reactToChange() is subscribed to the store
Each time an action is dispatched, 
reactToChange() is called and prints the current value of the light switch. 
It is common for callbacks subscribed to the store to use store.getState() inside them.
After the first two dispatched actions, 
unsubscribe() is called causing reactToChange() to no longer be exectued in response to further dispatches made to store.
Note: It is not always required to use the unsubscribe() function returned by store.subscribe(), 
though it is useful to know that it exists.

Now, take a look at store.js in the code editor.
You will see that a few actions have been dispatched to the store of the counter application. 
Suppose you wanted to print the current value of store.getState() each time the state changes. 
While you could write something like this…

store.dispatch(decrement());
console.log(`The count is ${store.getState()}`);
store.dispatch(increment());
console.log(`The count is ${store.getState()}`);
store.dispatch(increment());
console.log(`The count is ${store.getState()}`);
…we know that this approach is repetitive. Instead, 

# conclusion

Remember that 
you can subscribe a change listener to print out the current state in response to state changes automatically.
