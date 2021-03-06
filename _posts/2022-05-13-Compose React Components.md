---
Layout:
Title: "Compose React Components"
Date: 2022-05-13
Categories:
---

# Introduction

Today i have learned about how to Compose React Components
 with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface
(UI) of modern web applications.

# body
Rendering ES6 style class components within other components is no different than rendering the simple components you used in the last few challenges. You can render JSX elements, stateless functional components, and ES6 class components within other components.

there is TypesOfFood component already rendering a component called Vegetables. Also, there is the Fruits component in the code example below.

Now less nest two components inside of Fruits — first NonCitrus, and then Citrus.Next, nest the Fruits class component into the TypesOfFood component, below the h1 heading element and above Vegetables. The result should be a series of nested components, which uses two different component types.

<class Fruits extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h2>Fruits:</h2>
       
          <Citrus />
        <NonCitrus />  { /* This is where we changed the code */ }
      </div>
    );
  }
};

class TypesOfFood extends React.Component {
  constructor(props) {
     super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
       
          <Fruits /> { /* This is where we changed the code */ }
      
        <Vegetables />
      </div>
    );
  }
};>

# conclusion

 Both of these NonCitrus and Citrus components are provided for us behind the scenes and note that since we are using a vscode without
 react app we may not see the actual results. 