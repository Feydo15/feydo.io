---
Layout:
Title: "Create a Controlled Form with react"
Date: 2022-06-08
Categories:
---

# Introduction

Today i have learned about how to Create a Controlled Form with react
under the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a 
great tool to render the User Interface
(UI) of modern web applications.

# body

since we can control the internal state for certain elements like input and textarea, with React,it
makes them controlled components. This applies to other form elements as well, including the regular
 HTML form element.

 now less take the code below as example and create a controlled form:

The MyForm component is set up with an empty form with a submit handler. The submit handler will be called when the form is submitted.

We've added a button which submits the form. You can see it has the type set to submit indicating it is the button controlling the form. Add the input element in the form and set its value and onChange() attributes. You should then complete the handleSubmit method so that it sets the component state property submit to the current input value in the local state.

Note: You also must call event.preventDefault() in the submit handler, to prevent the default form submit behavior which will refresh the web page. For camper convenience, the default behavior has been disabled here to prevent refreshes from resetting challenge code.

Finally, create an h1 tag after the form which renders the submit value from the component's state. You can then type in the form and click the button (or press enter), and you should see your input rendered to the page.

<class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      submit: ''
    };
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  handleSubmit(event) {
    event.preventDefault()
    this.setState({
      submit: this.state.input
    });
  }
  render() {
    return (
      <div>
        <form onSubmit={this.handleSubmit}>
          <input
            value={this.state.input}
            onChange={this.handleChange} />
          <button type='submit'>Submit!</button>
        </form>
        <h1>{this.state.submit}</h1>
      </div>
    );
  }
};>

# conclusion

Please note that  we cant really see the DOM since we are using the 
vs code that has no react app template installed
on it and most of the components we used are assumed to be created in the background.
