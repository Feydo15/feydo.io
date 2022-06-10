---
Layout:
Title: "Create a React Component"
Date: 2022-05-06
Categories:
---

# Introduction

Today i have learned about to Create a React Component with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface
(UI) of modern web applications.

# body

The other way to define a React component is with the ES6 class syntax. In the following example, Kitten extends React.Component:

class Kitten extends React.Component {
constructor(props) {
super(props);
}

render() {
return (
<h1>Hi</h1>
);
}
This creates an ES6 class Kitten which extends the React.Component class. So the Kitten class now has access to many useful React features, such as local state and lifecycle hooks. Don't worry if you aren't familiar with these terms yet, they will be covered in greater detail in later challenges. Also notice the Kitten class has a constructor defined within it that calls super(). It uses super() to call the constructor of the parent class, in this case React.Component. The constructor is a special method used during the initialization of objects that are created with the class keyword. It is best practice to call a component's constructor with super, and pass props to both. This makes sure the component is initialized properly.
}

now less complete this code example below and finish writing the render method so it returns a div element that contains an h1 with the text Hello React!.:

class MyComponent extends React.Component {
constructor(props) {
super(props);
}
render() {

return <div>

         <h1>Hello React!</h1>
        </div>

}
};

# conclusion

For now, know that it is standard for this code to be included. Soon you will see other uses for the constructor as well as props.
