---
Layout:
Title: "Display Shapes with SVG"
Date: 2022-07-28
Categories:
---

# Introduction
today i have learned about how to Display Shapes with SVG under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body
given svg element with a given width and height, which is visible because it has a background-color applied to it in the style tag. The code makes space for the given width and height.
now we will create a shape to put in the svg area.

There are a number of supported shapes in SVG, such as rectangles and circles. They are used to display data. For example, a rectangle (<rect>) SVG shape could create a bar in a bar chart.

When you place a shape into the svg area, you can specify where it goes with x and y coordinates. The origin point of (0, 0) is in the upper-left corner. Positive values for x push the shape to the right, and positive values for y push the shape down from the origin point.

To place a shape in the middle of the 500 (width) x 100 (height) svg from last challenge, the x coordinate would be 250 and the y coordinate would be 50.

now less take the following code for example and Add a rect shape to the svg using append(), and give it a width attribute of 25 and height attribute of 100. Also, give the rect x and y attributes each set to 0.

<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    const w = 500;
    const h = 100;

    const svg = d3.select("body")
                  .append("svg")
                  .attr("width", w)
                  .attr("height", h)
                  // Add your code below this line

                  .append("rect")
                  .attr("width", 25)
                  .attr("height",100)
                  .attr("x",0)
                  .attr("y",0);


                  // Add your code above this line
  </script>
</body>

# conclusion
An SVG rect has four attributes. There are the x and y coordinates for where it is placed in the svg area. It also has a height
and width to specify the size.