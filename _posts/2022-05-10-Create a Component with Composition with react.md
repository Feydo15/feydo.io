---
Layout:
Title: "Create a Component with Composition with react"
Date: 2022-05-10
Categories:
---

# Introduction

Today i have learned about how to Create a Component with Composition with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface
(UI) of modern web applications.

# body

Now we will look at how we can compose multiple React components together. Imagine we are building an app and have created three components: a Navbar, Dashboard, and Footer.

To compose these components together, you could create an App parent component which renders each of these three components as children. To render a component as a child in a React component, you include the component name written as a custom HTML tag in the JSX. For example, in the render method you could write:

return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
)
When React encounters a custom HTML tag that references another component (a component name wrapped in < /> like in this example), it renders the markup for that component in the location of the tag. This should illustrate the parent/child relationship between the App component and the Navbar, Dashboard, and Footer.

now less complete this code example below there is a simple functional component called ChildComponent and a class component called ParentComponent.we need to Compose the two together by rendering the ChildComponent within the ParentComponent and Make sure to close the ChildComponent tag with a forward slash.

<const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        <ChildComponent/>

      </div>
    );
  }
};>

# conclusion
ChildComponent is defined with an ES6 arrow function because this is a very common practice when using React. However, know that this is just a function. If you aren't familiar with the arrow function syntax, please refer to the JavaScript section.