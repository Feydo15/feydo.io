---
Layout:
Title: "Write a Simple Counter with react"
Date: 2022-06-06
Categories:
---

# Introduction

Today i have learned about how to Write a Simple Counter with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

so far i can design a more complex stateful component by combining the concepts covered so far. These include initializing state, writing methods that set state, and assigning click handlers to trigger these methods.

now less take the code below example :
The Counter component keeps track of a count value in state. There are two buttons which call methods increment() and decrement(). Write these methods so the counter value is incremented or decremented by 1 when the appropriate button is clicked. Also, create a reset() method so when the reset button is clicked, the count is set to 0.

Note: Make sure you don't modify the classNames of the buttons. Also, remember to add the necessary bindings for the newly-created methods in the constructor. 

<class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
    // Change code below this line
this.increment=this.increment.bind(this)
this.decrement=this.decrement.bind(this)
this.reset=this.reset.bind(this)
    // Change code above this line
  }
  // Change code below this line
increment(){
  this.setState((state, props)=>{
    return{count:state.count + 1}
  })
}

decrement(){
  this.setState((state, props)=>{
    return{count:state.count - 1}
  })
}

reset(){
  this.setState((state, props)=>{
    return{count: 0}
  })
}

  // Change code above this line
  render() {
    return (
      <div>
        <button className='inc' onClick={this.increment}>Increment!</button>
        <button className='dec' onClick={this.decrement}>Decrement!</button>
        <button className='reset' onClick={this.reset}>Reset</button>
        <h1>Current Count: {this.state.count}</h1>
      </div>
    );
  }
};>
# conclusion

Please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
