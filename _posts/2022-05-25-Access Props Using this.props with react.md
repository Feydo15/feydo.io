---
Layout:
Title: "Access Props Using this.props with react"
Date: 2022-05-25
Categories:
---

# Introduction

Today i have learned about how to Access Props Using this.props with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

 what if the child component that we're passing a prop to is an ES6 class component, rather than a stateless functional component? The ES6 class component uses a slightly different convention to access props.

 Anytime we refer to a class component within itself, we use the this keyword. To access props within a class component, we preface the code that we use to access it with this. For example, if an ES6 class component has a prop called data, we write {this.props.data} in JSX.

 Now less take the code below for example and render an instance of the Welcome component in the parent component App. Here, give Welcome a prop of name and assign it a value of a string. Within the child, Welcome, access the name prop within the strong tags.

.


 class App extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
            { /* Change code below this line */ }
            <Welcome name={"james"} />
            { /* Change code above this line */ }
        </div>
    );
  }
};

class Welcome extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
          { /* Change code below this line */ }
          <p>Hello, <strong>{this.props.name}</strong>!</p>
          { /* Change code above this line */ }
        </div>
    );
  }
};

# conclusion
please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
