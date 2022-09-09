---
Layout:
Title: "Add Classes with D3"
Date: 2022-07-21
Categories:
---

# Introduction
today i have learned about how to Add Classes with D3 under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body
Using a lot of inline styles on HTML elements gets hard to manage, even for smaller apps. It's easier to add a class to elements and style that class one time using CSS rules. D3 has the attr() method to add any HTML attribute to an element, including a class name.

The attr() method works the same way that style() does. It takes comma-separated values, and can use a callback function. Here's an example to add a class of container to a selection:

selection.attr("class", "container");

now less take the code below for example and Add the attr() method to the code in the editor and put a class of bar on the div elements.
 
 <style>
  .bar {
    width: 25px;
    height: 100px;
    display: inline-block;
    background-color: blue;
  }
</style>
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    d3.select("body").selectAll("div")
      .data(dataset)
      .enter()
      .append("div")
      // Add your code below this line
       .attr("class", "bar");


      // Add your code above this line
  </script>
</body>

# conclusion
Note that the class parameter will remain the same whenever you need to add a class and only the container parameter will change.

