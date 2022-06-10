---
Layout:
Title: 'Create a Stateless Functional Component'
Date: 2022-05-05
Categories:
---

# Introduction

Today i have learned about to Create a Stateless Functional Component with react 
 under the Front End Development Libraries.
 React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface 
 (UI) of modern web applications.

# body

Components are the core of React. Everything in React is a component and here you will learn how to create one.

There are two ways to create a React component. The first way is to use a JavaScript function. Defining a component in this way creates a stateless functional component. For now, think of a stateless component as one that can receive data and render it, but does not manage or track changes to that data.

To create a component with a function, you simply write a JavaScript function that returns either JSX or null. One important thing to note is that React requires your function name to begin with a capital letter. Here's an example of a stateless functional component that assigns an HTML class in JSX:

const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};
After being transpiled, the <div> will have a CSS class of customClass.

Because a JSX component represents HTML, you could put several components together to create a more complex HTML page. This is one of the key advantages of the component architecture React provides. It allows you to compose your UI from many separate, isolated components. This makes it easier to build and maintain complex user interfaces.

now less complete this code example below so it returns a single div element which contains some string of text:
<const MyComponent = function(){
    return <div>"Hello world"</div>
}>

# conclusion
The text is considered a child of the div element, so you will not be able to use a self-closing tag.