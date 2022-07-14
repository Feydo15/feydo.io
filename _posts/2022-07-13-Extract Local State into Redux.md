---
Layout:
Title: "Extract Local State into Redux"
Date: 2022-07-13
Categories:
---

# Introduction
today i have learned about how to Extract Local State into Redux under React and Redux.
 Redux can be used within the context of any UI framework, 
though it is most commonly paired with React. This makes sense considering that React 
and Redux were both developed by engineers at Facebook.

# body

Now that Redux is connected, we need to extract the state management out of the Presentational component and into Redux. Currently, we have Redux connected, but we are handling the state locally within the Presentational component.

In the Presentational component, first, remove the messages property in the local state. These messages will be managed by Redux. Next, modify the submitMessage() method so that it dispatches submitNewMessage() from this.props, and pass in the current message input from local state as an argument. Because you removed messages from local state, remove the messages property from the call to this.setState() here as well. Finally, modify the render() method so that it maps over the messages received from props rather than state.

Once these changes are made, the app will continue to function the same, except Redux manages the state. This example also illustrates how a component may have local state: our component still tracks user input locally in its own state. You can see how Redux provides a useful state management framework on top of React. You achieved the same result using only React's local state at first, and this is usually possible with simple apps.

less take this code for example:

<// Redux:
const ADD = 'ADD';

const addMessage = (message) => {
  return {
    type: ADD,
    message: message
  }
};

const messageReducer = (state = [], action) => {
  switch (action.type) {
    case ADD:
      return [
        ...state,
        action.message
      ];
    default:
      return state;
  }
};

const store = Redux.createStore(messageReducer);

// React:
const Provider = ReactRedux.Provider;
const connect = ReactRedux.connect;

// Change code below this line
class Presentational extends React.Component {
  constructor(props) {
    super(props);
    
    // Remove property 'messages' from Presentational's local state
    this.state = {
      input: ''
    }
    this.handleChange = this.handleChange.bind(this);
    this.submitMessage = this.submitMessage.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  submitMessage() {
  
    // Call 'submitNewMessage', which has been mapped to Presentational's props, with a new message;
    // meanwhile, remove the 'messages' property from the object returned by this.setState().
    this.props.submitNewMessage(this.state.input);
    this.setState({
      input: ''
    });
  }
  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>
        <input
          value={this.state.input}
          onChange={this.handleChange}/><br/>
        <button onClick={this.submitMessage}>Submit</button>
        <ul>
           {/* The messages state is mapped to Presentational's props; therefore, when rendering,
               you should access the messages state through props, instead of Presentational's
               local state. */}
          {this.props.messages.map( (message, idx) => {
              return (
                 <li key={idx}>{message}</li>
              )
            })
          }
        </ul>
      </div>
    );
  }
};
// Change code above this line

const mapStateToProps = (state) => {
  return {messages: state}
};

const mapDispatchToProps = (dispatch) => {
  return {
    submitNewMessage: (message) => {
      dispatch(addMessage(message))
    }
  }
};

const Container = connect(mapStateToProps, mapDispatchToProps)(Presentational);

class AppWrapper extends React.Component {
  render() {
    return (
      <Provider store={store}>
        <Container/>
      </Provider>
    );
  }
};>

# conclusion
 However, as our apps become larger and more complex, so does your state management, 
 and this is the problem Redux solves.