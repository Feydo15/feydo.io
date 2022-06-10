---
Layout:
Title: "Use PropTypes to Define the Props You Expect with react"
Date: 2022-05-24
Categories:
---

# Introduction

Today i have learned about how to Use PropTypes to Define the Props You Expect with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a
great tool to render the User Interface
(UI) of modern web applications.

# body

React provides useful type-checking features to verify that components receive props of the correct type. For example, your application makes an API call to retrieve data that you expect to be in an array, which is then passed to a component as a prop. You can set propTypes on your component to require the data to be of type array. This will throw a useful warning when the data is of any other type.

It's considered a best practice to set propTypes when you know the type of a prop ahead of time. You can define a propTypes property for a component in the same way you defined defaultProps. Doing this will check that props of a given key are present with a given type. Here's an example to require the type function for a prop called handleClick:

<MyComponent.propTypes = { handleClick: PropTypes.func.isRequired }>

In the example above, the PropTypes.func part checks that handleClick is a function. Adding isRequired tells React that handleClick is a required property for that component. You will see a warning if that prop isn't provided. Also notice that func represents function. Among the seven JavaScript primitive types, function and boolean (written as bool) are the only two that use unusual spelling. In addition to the primitive types, there are other types available. For example, you can check that a prop is a React element. Please refer to the documentation for all of the options.

Less take the code below for example and Define propTypes for the Items component to require quantity as a prop and verify that it is of type number.

const Items = (props) => {
return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
};

// Change code below this line
Items.propTypes = { quantity: PropTypes.number.isRequired }
// Change code above this line

Items.defaultProps = {
quantity: 0
};

class ShoppingCart extends React.Component {
constructor(props) {
super(props);
}
render() {
return <Items />
}
};

# conclusion

Note: As of React v15.5.0, PropTypes is imported independently from React, like this: import PropTypes from 'prop-types';
please note that we cant really see the DOM since we are using the
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
