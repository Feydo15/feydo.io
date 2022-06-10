---
Layout:
Title: "Create a Stateful Component with react"
Date: 2022-05-27
Categories:
---

# Introduction

Today i have learned about how to Create a Stateful Component with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body
One of the most important topics in React is state. State consists of any data your application needs to know about, that can change over time. You want your apps to respond to state changes and present an updated UI when necessary. React offers a nice solution for the state management of modern web applications.

You create state in a React component by declaring a state property on the component class in its constructor. This initializes the component with state when it is created. The state property must be set to a JavaScript object. Declaring it looks like this:

this.state = {

}

You have access to the state object throughout the life of your component. You can update it, render it in your UI, and pass it as props to child components. The state object can be as complex or as simple as you need it to be.

There is a component in the code below that is trying to render a name property from its state. However, there is no state defined. Initialize the component with state in the constructor and assign your name to a property of name.
less do this :

<class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    // Only change code below this line
this.state ={
  name: ""
}
    // Only change code above this line
  }
  render() {
    return (
      <div>
        <h1>{this.state.name}</h1>
      </div>
    );
  }
};>

# conclusion
Note that you must create a class component by extending React.Component in order to create state like this.
Please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
