---
Layout:
Title: "Create a Bar for Each Data Point in the Set"
Date: 2022-07-25
Categories:
---

# Introduction
today i have learned about how to Create a Bar for Each Data Point in the Set under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body
On our code we only have one rectangle on the svg element to represent a bar. Here, we'll combine  data(), enter(), and SVG shapes to create and append a rectangle for each data point in dataset.

we will use the format for how to create and append a div for each item in dataset:

d3.select("body").selectAll("div")
  .data(dataset)
  .enter()
  .append("div")
There are a few differences working with rect elements instead of div elements. The rect elements must be appended to an svg element, not directly to the body. Also, you need to tell D3 where to place each rect within the svg area. The bar placement will be covered in the next challenge.

now less take this code for example: and Use the data(), enter(), and append() methods to create and append a rect for each item in dataset. The bars should display all on top of each other.

<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h);

    svg.selectAll("rect")
       // Add your code below this line
 
  .data(dataset)
  .enter()
  .append("rect")



       // Add your code above this line
       .attr("x", 0)
       .attr("y", 0)
       .attr("width", 25)
       .attr("height", 100);
  </script>
</body>

# conclusion
