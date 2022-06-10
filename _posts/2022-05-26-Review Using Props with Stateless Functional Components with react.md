---
Layout:
Title: "Review Using Props with Stateless Functional Components with react"
Date: 2022-05-26
Categories:
---

# Introduction

Today i have learned about how to Review Using Props with Stateless Functional Components with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body
 when passing props to stateless functional components these components act like pure functions. They accept props as input and return the same view every time they are passed the same props. You may be wondering what state is, here's a review of the terminology for components.

 A stateless functional component is any function you write which accepts props and returns JSX. A stateless component, on the other hand, is a class that extends React.Component, but does not use internal state. Finally, a stateful component is a class component that does maintain its own internal state. You may see stateful components referred to simply as components or React components.

A common pattern is to try to minimize statefulness and to create stateless functional components wherever possible. This helps contain your state management to a specific area of your application. In turn, this improves development and maintenance of your app by making it easier to follow how changes to state affect its behavior.

less take the code below for example and Define the Camper component and assign it default props of { name: 'CamperBot' }. Inside the Camper component, render any code that you want, but make sure to have one p element that includes only the name value that is passed in as a prop. Finally, define propTypes on the Camper component to require name to be provided as a prop and verify that it is of type string.

class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <Camper />
      </div>
    );
  }
};
// Change code below this line

const Camper = (props) => {
return <p>{props.name}</p>}

Camper.propTypes = { name: PropTypes.string.isRequired }

Camper.defaultProps = { name: 'CamperBot' }

# conclusion

please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
