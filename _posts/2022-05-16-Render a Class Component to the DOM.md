---
Layout:
Title: "Render a Class Component to the DOM"
Date: 2022-05-16
Categories:
---

# Introduction

Today i have learned about how to Render a Class Component to the DOM
with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a
great tool to render the User Interface
(UI) of modern web applications.

# body

Here's a refresher on the syntax: ReactDOM.render(componentToRender, targetNode). The first argument is the React component that we want to render. The second argument is the DOM node that we want to render that component within.

React components are passed into ReactDOM.render() a little differently than JSX elements. For JSX elements, we pass in the name of the element that we want to render. However, for React components, we need to use the same syntax as if you were rendering a nested component, for example ReactDOM.render(<ComponentToRender />, targetNode). we use this syntax for both ES6 class components and functional components.

less say both Fruits and Vegetables components are defined for us behind the scenes, Now less Render both components as children of the TypesOfFood component then render TypesOfFood to the DOM. there is a div with Id="challenge-node" available for us to use.

<class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* now less Render the children components below this line */}
       
        <Fruits />
        <Vegetables />
     
      </div>
    );
  }
};

// now less Render the parent component  below this line>

ReactDOM.render(<TypesOfFood />, document.getElementById("challenge-node"))

# conclusion

note that we cant really see the DOM since we are using the vs code that has no react app template 
installed on it and most of the components we used are assumed to be created in the background.