---
Layout:
Title: "How to write action creators in redux"
Date: 2022-06-29
Categories:
---

# Introduction
today i have learned about how to write action creator in redux.
action creators are used to reduce the repetition of  dispatch actions of the same type from  multiple places which may lead to an  opportunities to make an error and  provide consistency.

# body

Action Creators

As you saw in the last exercise, 
you are likely to dispatch actions of the same type multiple times or from multiple places. 
Typing out the entire action object can be tedious and creates opportunities to make an error.

For example, in the light switch application, 
whose reducer accepts 'toggle' actions to turn the light 'on' or 'off', you might write:

store.dispatch({Type:'toggle'});
store.dispatch({type:'toggel'});
store.dispatch({typo:'toggle'});
Did you spot the errors?

In most Redux applications, 
action creators are used to reduce this repetition and to provide consistency. 
An action creator is simply a function that returns an action object with a type property. 
They are typically called and passed directly to the
 store.dispatch() method resulting in fewer errors and an easier-to-read dispatch statement.

The above code could be rewritten using an action creator called toggle() like so:

const toggle = () => {
  return { type: "toggle" };
}
store.dispatch(toggle()); // Toggles the light to 'off'
store.dispatch(toggle()); // Toggles the light back to 'on'
store.dispatch(toggle()); // Toggles the light back to 'off'
Though not necessary in a Redux application, 
action creators save us the time needed to type out the entire action object, 
reduce the chances you make a typo, and improve the readability of our application.

# conclusion

Often, before the reducer of an application is even written, 
Redux programmers will write action creators as a way of planning out which actions will be 
available to dispatch to the store.