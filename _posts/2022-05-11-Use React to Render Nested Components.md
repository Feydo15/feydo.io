---
Layout:
Title: "Use React to Render Nested Components"
Date: 2022-05-11
Categories:
---

# Introduction

Today i have learned about how to Use React to Render Nested Components with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface
(UI) of modern web applications.

# body

there are many different ways you can compose components with React.

Component composition is one of React's powerful features. When you work with React, it is important to start thinking about your user interface in terms of components like the App example in the last challenge. You break down your UI into its basic building blocks, and those pieces become the components. This helps to separate the code responsible for the UI from the code responsible for handling your application logic. It can greatly simplify the development and maintenance of complex projects.

There are two functional components defined in the code example below, called TypesOfFruit and Fruits.less take the TypesOfFruit component and compose it, or nest it, within the Fruits component. Then take the Fruits component and nest it within the TypesOfFood component. The result should be a child component, nested within a parent component, which is nested within a parent component of its own!

<const TypesOfFruit = () => {
return (
<div>
<h2>Fruits:</h2>
<ul>
<li>Apples</li>
<li>Blueberries</li>
<li>Strawberries</li>
<li>Bananas</li>
</ul>
</div>
);
};

const Fruits = () => {
return (
<div>
<TypesOfFruit /> { /_ this is where we changed the code_/ }

    </div>

);
};

class TypesOfFood extends React.Component {
constructor(props) {
super(props);
}

render() {
return (
<div>
<h1>Types of Food:</h1>

<Fruits /> { /_ this is where we changed the code_/ }

      </div>
    );

}
};>

# conclusion

in react we can nest components in one another like child to parent that is also nested in the parent on its own.
