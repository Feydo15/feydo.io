---
Layout:
Title: "Change Styles Based on Data"
Date: 2022-07-21
Categories:
---

# Introduction
today i have learned about how to Change Styles Based on Data under Data 
Visualization with D3.
D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for 
creating dynamic and interactive data visualizations in the browser.
D3 is built to work with common web standards – namely HTML, CSS, and Scalable 
Vector Graphics (SVG).

# body

D3 is about visualization and presentation of data. It's likely you'll want to change the styling of elements based on the data. You can use a callback function in the style() method to change the styling for different elements.

For example, you may want to color a data point blue if it has a value less than 20, and red otherwise. You can use a callback function in the style() method and include the conditional logic. The callback function uses the d parameter to represent the data point:

selection.style("color", (d) => {

});

now less take the code below for example and Add the style() method to the code in the editor to set the color of the h2 elements conditionally. Write the callback function so if the data value is less than 20, it returns red, otherwise it returns green.

<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

    d3.select("body").selectAll("h2")
      .data(dataset)
      .enter()
      .append("h2")
      .text((d) => (d + " USD"))
      // Add your code below this line
.style("color", (d) => {
 if(d < 20){
   return "red"
 }else{
   return "green"
 }
});

      // Add your code above this line
  </script>
</body>

Note: You can use if-else logic, or the ternary operator.

# conclusion
note:The style() method is not limited to setting the color - it can be used with other CSS properties as well.
