---
Layout:
Title: "React Props"
Date: 2022-09-21
Categories:
---

# Introduction
today i have learned about React Props.
React Props are like function arguments in JavaScript and attributes in HTML.
and to send props into a component, use the same syntax as HTML attributes

# body

Props are also how you pass data from one component to another, as parameters.
if we are sending a variable to another component and it is not a string we just 
put the variable name inside curly brackets
just like in the example below:

Create a variable named carName and send it to the Car component:
<function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  const carName = "Ford";
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carName } />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);>

the nex example is for passing data from one component as an object to another
Create an object named carInfo and send it to the Car component:
function Car(props) {
  return <h2>I am a { props.brand.model }!</h2>;
}

function Garage() {
  const carInfo = { name: "Ford", model: "Mustang" };
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carInfo } />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);

# conclusion
Note: React Props are read-only! You will get an error if you try to change their value.
