---
Layout:
Title: 'Render HTML Elements to the DOM'
Date: 2022-05-02
Categories:
---

# Introduction

Today i have learned about how to Render HTML Elements to the DOM with react under
the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface 
(UI) of modern web applications.

# body
With React, we can render this JSX directly to the HTML DOM using React's rendering API known as ReactDOM.

ReactDOM offers a simple method to render React elements to the DOM which looks like this: ReactDOM.render(componentToRender, targetNode), where the first argument is the React element or component that you want to render, and the second argument is the DOM node that you want to render the component to.

As you would expect, ReactDOM.render() must be called after the JSX element declarations, just like how you must declare variables before using them.

now less use the ReactDOM.render() method to render this component to the page. we can pass defined JSX elements directly in as the first argument and use document.getElementById() to select the DOM node to render them to.less use this div with id='challenge-node' and make sure we don't change the JSX constant.
<const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);>

<ReactDOM.render(JSX ,document.getElementById("challenge-node"))>

# conclusion
on our code 
The constant JSX should return a div element.
The div should contain an h1 tag as the first element.
The div should contain a p tag as the second element.
The provided JSX element should render to the DOM node with id challenge-node.
