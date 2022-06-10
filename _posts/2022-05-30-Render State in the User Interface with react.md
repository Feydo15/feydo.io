---
Layout:
Title: "Render State in the User Interface with react"
Date: 2022-05-30
Categories:
---

# Introduction

Today i have learned about how to Render State in the User Interface with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

state is one of the most powerful features of components in React. It allows you to track important data in your app and render a UI in response to changes in this data. If your data changes, your UI will change. React uses what is called a virtual DOM, to keep track of changes behind the scenes. When state data updates, it triggers a re-render of the components using that data - including child components that received the data as a prop. React updates the actual DOM, but only where necessary. This means you don't have to worry about changing the DOM. You simply declare what the UI should look like.

Note that if you make a component stateful, no other components are aware of its state. Its state is completely encapsulated, or local to that component, unless you pass state data to a child component as props. This notion of encapsulated state is very important because it allows you to write certain logic, then have that logic contained and isolated in one place in your code.

Once you define a component's initial state, you can display any part of it in the UI that is rendered. If a component is stateful, it will always have access to the data in state in its render() method. You can access the data with this.state.

If you want to access a state value within the return of the render method, you have to enclose the value in curly braces.

Now less take the code below for example and define an h1 tag in the component's render method which renders the value of name from the component's state.MyComponent is already stateful.
Note: The h1 should only render the value from state and nothing else. In JSX, any code you write with curly braces { } will be treated as JavaScript. So to access the value from state just enclose the reference in curly braces.

<class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    return (
      <div>
                                    
         <h1>{this.state.name}</h1>         { /* we changed the code on this line */ }
        
      </div>
    );
  }
};>


# conclusion
Please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
