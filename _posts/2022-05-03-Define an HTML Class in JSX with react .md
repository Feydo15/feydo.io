---
Layout:
Title: 'Define an HTML Class in JSX with react'
Date: 2022-05-03
Categories:
---

# Introduction

Today i have learned about how to Define an HTML Class in JSX with react 
 under the Front End Development Libraries.
 React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface 
(UI) of modern web applications.

# body

first less check the difference between jsx and HTML.  
One key difference in JSX is that you can no longer use the word class to define HTML classes. This is because class is a reserved word in JavaScript. Instead, JSX uses className.

In fact, the naming convention for all HTML attributes and event references in JSX become camelCase. For example, a click event in JSX is onClick, instead of onclick. Likewise, onchange becomes onChange. While this is a subtle difference, it is an important one to keep in mind moving forward.

now less apply a class to the div element on this  jsx example :

|<const JSX = (
  <div className="myDiv">
    <h1>Add a class to this div</h1>
  </div>
);>

# conclusion

IN HTML we use use just the word class but in JSX we use the  word className and keep in mind 
that it should be written in camelCase at all the time.