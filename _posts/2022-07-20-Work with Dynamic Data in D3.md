---
Layout:
Title: "Work with Dynamic Data in D3"
Date: 2022-07-20
Categories:
---

# Introduction
today i have learned about how to Work with Dynamic Data in D3 under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body
 Now we know the basics of displaying data dynamically with D3 using the data() and enter() methods. These methods take a data set and, together with the append() method, create a new DOM element for each entry in the data set.

we have created a new h2 element for each item in the dataset array, but they all contained the same text, New Title. This is because you have not made use of the data that is bound to each of the h2 elements.

The D3 text() method can take a string or a callback function as an argument:

selection.text((d) => d)
In the example above, the parameter d refers to a single entry in the dataset that a selection is bound to.

Using the current example as context, the first h2 element is bound to 12, the second h2 element is bound to 31, the third h2 element is bound to 22, and so on.

now less take the code below and change the text() method so that each h2 element displays the corresponding value from the dataset array with a single space and the string USD. For example, the first heading should be 12 USD.

<<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];
    
    d3.select("body").selectAll("h2")
      .data(dataset)
      .enter()
      .append("h2")
      
      .text((d) => `${d} USD`);
      
  </script>
</body>    >

# conclusion
The D3 text() method can take a string or a callback function as an argument: