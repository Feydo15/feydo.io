---
Layout:
Title: "Pass an Array as Props with react"
Date: 2022-05-19
Categories:
---

# Introduction

Today i have learned about how to Pass an Array as Props with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body
 To pass an array to a JSX element, it must be treated as JavaScript and wrapped in curly braces.
 <ParentComponent>
  <ChildComponent colors={["green", "blue", "red"]} />
</ParentComponent>

The child component then has access to the array property colors. Array methods such as join() can be used when accessing the property. const ChildComponent = (props) => <p>{props.colors.join(', ')}</p> This will join all colors array items into a comma separated string and produce: <p>green, blue, red</p>

There are List and ToDo components in the code below. When rendering each List from the ToDo component, pass in a tasks property assigned to an array of to-do tasks, for example ["walk dog", "workout"]. Then access this tasks array in the List component, showing its value within the p element. Use join(", ") to display the props.tasksarray in the p element as a comma separated list. Today's list should have at least 2 tasks and tomorrow's should have at least 3 tasks.

Now less this code below as an example this example:

const List = (props) => {
  { /* Change code below this line */ }
  return <p>{props.tasks.join(', ')}</p>
  { /* Change code above this line */ }
};

class ToDo extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>To Do Lists</h1>
        <h2>Today</h2>
        { /* Change code below this line */ }
        <List tasks={["walk dog", "workout","sleep"]}/>
        <h2>Tomorrow</h2>
        <List tasks={["walk dog", "workout","eat","dance"]}/>
        { /* Change code above this line */ }
      </div>
    );
  }
};

# conclusion
note that we cant really see the DOM since we are using the vs code that has no react app template 
installed on it and most of the components we used are assumed to be created in the background.