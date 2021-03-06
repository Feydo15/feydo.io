---
Layout:
Title: "Use @if and @else to Add Logic To Your Styles"
Date: 2022-04-20
Categories:
---

# Introduction

Today i have learned about how to Use @if and @else to Add Logic To Your Styles
under
the Front End Development Libraries.

# body

The @if directive in Sass is useful to test for a specific case - it works just like the if statement in JavaScript.

<@mixin make-bold($bool) {
  @if $bool == true {
    font-weight: bold;
  }
}>
And just like in JavaScript, @else if and @else test for more conditions:<@mixin text-effect($val) {
@if $val == danger {
color: red;
}
@else if $val == alert {
color: yellow;
}
@else if $val == success {
color: green;
}
@else {
color: black;
}
}>

now less Create a mixin called border-stroke that takes a parameter $val. The mixin should check for the following conditions using @if, @else if, and @else:

we first need to write our #box div like this.

<?<div id="box"></div>
>
then in our style element we create our @mixin like this:
<<style type='text/sass'>
  @mixin border-stroke($val) {
    @if $val == light {
      border: 1px solid black;
    }
    @else if $val == medium {
      border: 3px solid black;
    }
    @else if $val == heavy {
      border: 6px solid black;
    }
    @else {
      border: none;
    }
  }
  
  #box {
    width: 150px;
    height: 150px;
    background-color: red;
    @include border-stroke(medium);
  }  
</style>>

# conclusion
this will change the color based on the conditions or statements that are set on the mixin.
