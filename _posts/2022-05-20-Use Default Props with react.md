---
Layout:
Title: "Use Default Props with react"
Date: 2022-05-20
Categories:
---

# Introduction

Today i have learned about how to Use Default Props with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

React also has an option to set default props. We can assign default props to a component as a property on the component itself and React assigns the default prop if necessary. This allows us to specify what a prop value should be if no value is explicitly provided. For example, if we declare MyComponent.defaultProps = { location: 'San Francisco' }, we have defined a location prop that's set to the string San Francisco, unless you specify otherwise. React assigns default props if props are undefined, but if you pass null as the value for a prop, it will remain null.

less take this code below for example :

This code shows a ShoppingCart component. less define default props on this component which specify a prop items with a value of 0.

<const ShoppingCart = (props) => {
  return (
    <div>
      <h1>Shopping Cart Component</h1>
    </div>
  )
};
// Change code below this line

ShoppingCart.defaultProps= {items: 0}>

# conclusion
note that the defaultProps also helps if the props passed are undefined but if we set it to be null 
it will remain null unless changed.