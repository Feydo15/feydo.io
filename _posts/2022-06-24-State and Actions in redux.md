---
Layout:
Title: "State and Actions in Redux"
Date: 2022-06-17
Categories:
---

# Introduction

Today i have learned about how to initialize state and create actions in redux 
State is the current information behind a web application.
Actions are the only source of information for the store as per Redux official documentation.

# body

State

For a calendar application it includes the events (name, date, label, etc.), the current timezone,
and the display filters. For a todo app it includes the todo items (description, completed/not completed),
the current order of the items, and display filters. For a word editor, it includes the contents of the document,
the print settings, and comments.

With Redux, state can be any JavaScript type, including: number, string, boolean, array, and object.

Here’s an example state for a todo app:

<const state = [ 'Print trail map', 'Pack snacks', 'Summit the mountain' ];>

Each piece of information in this state—an array in this case—would inform some part of the user interface.


******************************************Actions******************************************

Most well-designed applications will have separate components that need to communicate and share data with each ot

A todo list might have an input field where the user can type in a new todo item.
The application might transfer this data from the input field, add it to an array of all todo's, 
and then render them as text on the screen. This entire interaction can be defined as an action. 
In Redux, actions are represented as plain JS objects.

Here’s what that action might look like:

const action = {
  type: 'todo's/addTodo',
  payload: 'Take selfies'
};
Every action must have a type property with a string value. This describes the action.

Typically, an action has a payload property with an object value.

This includes any information related to the action. In this case, 
the payload is the todo text.

When an action is generated and notifies other parts of the application, 
we say that the action is dispatched.

Here are two more example actions:

“Remove all todo's”. This requires no payload because no additional information is needed:

const action = {
  type: 'todo's/removeAll'
}
“Remove the ‘Pack snacks’ todo”:

const action = {
  type: 'todo's/removeTodo',
  payload: 'Pack snacks'

  # conclusion
  state and actions are part of redux flow that works together with store and reducers 
  we cant really see them in action since we are using them on a vscode that has no redux 
