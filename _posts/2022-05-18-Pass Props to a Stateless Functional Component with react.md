---
Layout:
Title: 'Pass Props to a Stateless Functional Component with react'
Date: 2022-05-18
Categories:
---

# Introduction

Today i have learned about how to Pass Props to a Stateless Functional Component with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a
great tool to render the User Interface
(UI) of modern web applications.

# body

In React, we can pass props, or properties, to child components. Say we have an App component which renders a child component called Welcome which is a stateless functional component. We can pass Welcome a user property by writing:

<App>
  <Welcome user='Mark' />
</App>

We use custom HTML attributes created by us and supported by React to be passed to the component. In this case, the created property user is passed to the component Welcome. Since Welcome is a stateless functional component, it has access to this value like so:

const Welcome = (props) => <h1>Hello, {props.user}!</h1>
It is standard to call this value props and when dealing with stateless functional components, we basically consider it as an argument to a function which returns JSX. We can access the value of the argument in the function body. With class components, we will see this is a little different.

There are Calendar and CurrentDate components in the code editor. When rendering CurrentDate from the Calendar component, pass in a property of date assigned to the current date from JavaScript's Date object. Then access this prop in the CurrentDate component, showing its value within the p tags. Note that for prop values to be evaluated as JavaScript, they must be enclosed in curly brackets, for instance date={Date()}.

const CurrentDate = (props) => {
return (
<div>
{ /_ we pass the date as a prop below this line _/ }
<p>The current date is: {props.date}</p>
  
 </div>
);
};

class Calendar extends React.Component {
constructor(props) {
super(props);
}
render() {
return (
<div>
<h3>What date is it?</h3>
{ /_ We render the date as a prop below this line _/ }
<CurrentDate date={Date()}/>
</div>
);
}
};

# conclusion

note that the current date on the p element will appear on the DOM but we cant really see the DOM since we are using the vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
