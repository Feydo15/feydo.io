---
Layout:
Title: "Filtering Arrays in React"
Date: 2022-09-21
Categories:
---

# Introduction
today i have learned about Filtering Arrays in React.
Filtering in React is pretty much what it says it is. It’s the process of looping through an array and including or excluding elements inside that array based on a condition that you provide.

# body

The caveat here is that we’re not actually filtering using React. Filter is a JavaScript function that we can perform on an array type object. Remember, we use JavaScript to write React. None of these methods are special to React. React is just the UI library.

less take this example 

Example: Filter an Array of Strings in React
This first example is quite a common scenario. Picture the scene: you’re creating a search filter component to allow your users to search a list of names.

Your users type into a text field to filter that array of names based on what they’re typing into that text field. It’s quite a common input element these days.

Let’s start off with a hard-coded array of strings. Names that you might recognize (plus a small addition):

const names = ['James', 'John', 'Paul', 'Ringo', 'George'];
Let’s assume that you want to only display names that include the letter ‘J’ in them.

To do that, we use the filter function. We can perform the filter function inside of our JSX in a React component like so:
<div>
  {names.filter(name => name.includes('J')).map(filteredName => (
    <li>
      {filteredName}
    </li>
  ))}
</div>

Let’s break down the code above.

First, we define our JSX inside by opening a new curly bracket inside of a <div> element. Then, we specify the array for which we want to perform the filter function on.

Because we are performing a function we open up a set of parentheses. This is where we want to set our condition for the filter: in this case, if the element in the array includes the letter ‘J’.

# conclusion
Did you know that you can chain array function in JavaScript, such as filter, map, and reduce? This can save many lines of code, although it may be difficult to understand for those new to coding.
