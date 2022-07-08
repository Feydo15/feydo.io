---
Layout:
Title: "React and Redux"
Date: 2022-07-08
Categories:
---

# Introduction
today i have learned about how to Connect React and Redux.
 Redux can be used within the context of any UI framework, 
though it is most commonly paired with React. This makes sense considering that React 
and Redux were both developed by engineers at Facebook.

# body

We can be more specific about the common steps involved in connecting Redux to a React UI:

A render() function will be subscribed to the store to re-render the top-level React Component.
The top-level React component will receive the current value of store.getState() as a prop and use 
that data to render the UI.
Event listeners attached to React components will dispatch actions to the store.
Take a look at store.js in the code editor. Here, 
you can see the completed light switch application following this pattern.

The render() function is subscribed to the store.
store.getState() is passed as a prop called state to the <LightSwitch /> component.
The LightSwitch component displays the current state of the store, either 'on' or 'off', 
and adjusts the background colors accordingly.
The LightSwitch component declares a click handler that dispatches a toggle() action to the store.
Note 1: The prop name state isn’t a special React name and can be customized as the programmer sees 
fit. For example, lightSwitchState={store.getState()} would also be valid.


The steps for connecting Redux to a UI are followed:

Create a Redux store
Render the initial state of the application.
Subscribe to updates. Inside the subscription callback:
Get the current store state
Select the data needed by this piece of UI
Update the UI with the data
Respond to UI events by dispatching Redux actions

# conclusion

we need to implement the Counter app using a React UI so that we can understand how the state of the store is used by this application’s React 
components.