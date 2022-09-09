---
Layout:
Title: "Update the Height of an Element Dynamically"
Date: 2022-07-21
Categories:
---

# Introduction
today i have learned about how to Update the Height of an Element Dynamically under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body
The previous challenges covered how to display data from an array and how to add CSS classes. You can combine these lessons to create a simple bar chart. There are two steps to this:

1.Create a div for each data point in the array
2.Give each div a dynamic height, using a callback function in the style() method that sets height equal to the data value.

now less take the code below for example and Add the style() method to the code in the editor to set the height property for each element. Use a callback function to return the value of the data point with the string px added to it.

Add the style() method to the code in the editor to set the height property for each element. Use a callback function to return the value of the data point with the string px added to it.

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
      .attr("class", "bar")
      // Add your code below this line
      .style('height', d => `${d}px`)

      // Add your code above this line
  </script>
</body>

# conclusion

Recall the format to set a style using a callback function:

selection.style("cssProperty", (d) => d)
