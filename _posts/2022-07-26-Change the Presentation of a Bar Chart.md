---
Layout:
Title: "Change the Presentation of a Bar Chart"
Date: 2022-07-26
Categories:
---

# Introduction
today i have learned about how to Change the Presentation of a Bar Chart under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body

in a bar chart,there are a couple of formatting changes that could improve it:



Add space between each bar to visually separate them, which is done by adding a margin to the CSS for the bar class

Increase the height of the bars to better show the difference in values, which is done by multiplying the value by a number to scale the height

for example less : First, add a margin of 2px to the bar class in the style tag. Next, change the callback function in the style() method so it returns a value 10 times the original data value (plus the px).

<style>
  .bar {
    width: 25px;
    height: 100px;
    /* Add your code below this line */
     margin:2px;
    
    /* Add your code above this line */
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
      .style("height", (d) => (d * 10 + "px")) // Change this line
  </script>
</body>


# conclusion

Note: Multiplying each data point by the same constant only alters the scale. It's like zooming in, and it doesn't change the meaning of the underlying data.
