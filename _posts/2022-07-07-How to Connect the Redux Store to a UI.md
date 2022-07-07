---
Layout:
Title: "Connect the Redux Store to a UI"
Date: 2022-07-07
Categories:
---

# Introduction
today i have learned about how to Connect the Redux Store to a UI in 
redux.
The UI for this application should display the current count number and allow the user to increment 
or decrement this value using the buttons provided. Take a look at the connected web browser window 
and you can see that the elements for such an interface are present, but they haven’t been connected to the Redux store yet.

# body
Connecting a Redux store with any UI requires a few consistent steps, regardless of how the UI is implemented:

Create a Redux store
Render the initial state of the application.
Subscribe to updates. Inside the subscription callback:
Get the current store state
Select the data needed by this piece of UI
Update the UI with the data
Respond to UI events by dispatching Redux actions
These same steps are followed when building an interface using React, Angular, 
or jQuery. 
For now, we’ll create a very simple user interface for the counting application using the HTML DOM API.

Open up the index.html file and you can see the three HTML elements that are currently being rendered:

<p id='counter'>Waiting for current state.</p>
<button id='incrementer'>+</button>
<button id='decrementer'>-</button>
Now, open up store.js where you will find the pieces of Redux code that you have built throughout 
this lesson: the action creators increment() and decrement(), the reducer countReducer, 
and the store that ties it all together. Additionally, the following values have been added:

counterElement, incrementer, and decrementer: references to the HTML elements in index.html
render: A state-change listener for responding to changes to the store‘s state.
incrementerClicked and decrementerClicked: DOM event handlers for responding to the buttons being clicked by the user.

# conclusion
These new functions and elements will allow us to plug the Redux store into the UI in a more consistent manner.