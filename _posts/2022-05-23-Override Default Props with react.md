---
Layout:
Title: "Override Default Props with react"
Date: 2022-05-23
Categories:
---

# Introduction

Today i have learned about how to Override Default Props with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a
great tool to render the User Interface
(UI) of modern web applications.

# body

The ability to set default props is a useful feature in React. The way to override the default props is to explicitly set the prop values for a component.

less take this code below for example:
The ShoppingCart component now renders a child component Items. This Items component has a default prop quantity set to the integer 0. Override the default prop by passing in a value of 100 for quantity.

const Items = (props) => {
return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
}

Items.defaultProps = {
quantity: 0
}

class ShoppingCart extends React.Component {
constructor(props) {
super(props);
}
render() {
{ /_ Change code below this line _/ }
return <Items quantity={100} />

}
};

# conclusion

Note: Remember that the syntax to add a prop to a component looks similar to how you add HTML attributes. However, since the value for quantity is an integer, it won't go in quotes but it should be wrapped in curly braces. For example, {100}. This syntax tells JSX to interpret the value within the braces directly as JavaScript.and 
please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
