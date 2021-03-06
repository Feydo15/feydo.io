---
Layout:
Title: "Render State in the User Interface Another Way with react"
Date: 2022-05-31
Categories:
---

# Introduction

Today i have learned about how to Render State in the User Interface Another Way with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body
This is another way to access state in a component
In the render() method, before the return statement, you can write JavaScript directly. For example, you could declare functions, access data from state or props, perform computations on this data, and so on. Then, you can assign any data to variables, which you have access to in the return statement.

Now less take this code below as an example: 
In the MyComponent render method, define a const called name and set it equal to the name value in the component's state. Because you can write JavaScript directly in this part of the code, you don't have to enclose this reference in curly braces.

Next, in the return statement, render this value in an h1 tag using the variable name. Remember, you need to use the JSX syntax (curly braces for JavaScript) in the return statement.
<class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  render() {
    //we Changed code below this line
const name = this.state.name
    //we Changed code above this line
    return (
      <div>
        { /*we Changed code below this line */ }
<h1>{name}</h1>
        { /*we Changed code above this line */ }
      </div>
    );
  }
};>

# conclusion
Please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
