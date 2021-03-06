---
Layout:
Title: 'Self-Closing JSX Tags with react'
Date: 2022-05-04
Categories:
---

# Introduction

Today i have learned about Self-Closing JSX Tags with react 
 under the Front End Development Libraries.
 React is an Open Source view library created and maintained by Facebook. It's a great tool to render the User Interface 
 (UI) of modern web applications.

# body

important way in which JSX differs from HTML is in the idea of the self-closing tag.
In HTML, almost all tags have both an opening and closing tag: <div></div>; the closing tag always has a forward slash before the tag name that you are closing. However, there are special instances in HTML called “self-closing tags”, or tags that don’t require both an opening and closing tag before another tag can start.

For example the line-break tag can be written as <br> or as <br />, but should never be written as <br></br>, since it doesn't contain any content.

In JSX, the rules are a little different. Any JSX element can be written with a self-closing tag, and every element must be closed. The line-break tag, for example, must always be written as <br /> in order to be valid JSX that can be transpiled. A <div>, on the other hand, can be written as <div /> or <div></div>. The difference is that in the first syntax version there is no way to include anything in the <div />. You will see in later challenges that this syntax is useful when rendering React components.

now less fix the errors in the code example below so that it is valid JSX and successfully transpiles and Make sure we don't change any of the content - we only need to close tags where they are needed.
like this

const JSX = (
  <div>
    <h2>Welcome to React!</h2>
     <br />
    <p>Be sure to close all tags!</p>
    <hr />
  </div>
);

# conclusion
note in jsx most of the tags can self close unlike in html where we need the closing tags in most of the Elements
