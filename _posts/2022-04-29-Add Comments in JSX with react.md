---
Layout:
Title: 'Add Comments in JSX with react'
Date: 2022-04-29
Categories:
---

# Introduction

Today i have learned about how to Add Comments in JSX with react under
the Front End Development Libraries.
React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface 
(UI) of modern web applications.

# body
JSX is a syntax that gets compiled into valid JavaScript. Sometimes, for readability, you might need to add comments to your code. Like most programming languages, JSX has its own way to do this.

To put comments inside JSX, you use the syntax {/* */} to wrap around the comment text.

less take this code for example :
const JSX = (
  <div>
    <h1>This is a block of JSX</h1>
    <p>Here's a subtitle</p>
  </div>
);

now less  add a comment somewhere within the provided div element, without modifying the existing h1 or p elements.

const JSX = (
  <div>
    <h1>This is a block of JSX</h1>
    <p>Here's a subtitle</p>
    {/* comment*/}
  </div>
);

# conclusion

The JSX should use valid comment syntax like this {/* comment*/}