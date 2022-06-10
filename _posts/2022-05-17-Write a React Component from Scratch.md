---
Layout:
Title: "Write a React Component from Scratch"
Date: 2022-05-17
Categories:
---

# Introduction

Today i have learned about how to Write a React Component from Scratch with react 
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

Now less define a class MyComponent that extends React.Component. Its render method should return a div that contains an h1 tag with the text: My First React Component! in it. Use this text exactly, the case and punctuation matter. Make sure to call the constructor for your component, too.

Render this component to the DOM using ReactDOM.render(). There is a div with id='challenge-node' available for us to use.

<class MyComponent extends React.Component{
   constructor(props){
     super(props);
   }

   render() {
   return (
       <div>
       <h1>My First React Component!</h1>
       </div>
   );
   }
};
ReactDOM.render(<MyComponent /> , document.getElementById("challenge-node"));>

# conclusion

note that we cant really see the DOM since we are using the vs code that has no react app template 
installed on it and most of the components we used are assumed to be created in the background.