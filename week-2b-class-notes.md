# Responsive Images using the Sizes attribute

## Sizes Demo

[HTML 5 Picture tag demo using the size attribute](./week-2b/sizes-demo.html)

<hr>

<blockquote>

### Reference Material 

#### CSS Box Sizing

CSS Box Sizing is a "fix" added to newer versions of CSS. In the initial version of CSS, with total width of a box would grow once you added things like padding and borders. *This was very unintuitive, and very confusing for designers.* 

##### box-sizing: content-box;

For example, a div with a width: 600px; in the CSS would actually be **634px wide** if you gave it padding of 1rem (16px each for the left and right value = 32px) and a 1px border (1px on the left and right sides = 2px total).

This behavior is called "content-box" because the width of the text content inside the box stays at 600px.

##### box-sizing: border-box;

The "fix" is a CSS one-liner: box-sizing: border-box;

When using this in your CSS, the overall width of the box remains constant (ex: 600px) even when adding extra parameters like padding and borders.


[https://www.w3schools.com/css/css3_box-sizing.asp](https://www.w3schools.com/css/css3_box-sizing.asp)

</blockquote>

<blockquote>

### Reference Material

#### How to Use HTML5 “picture”, “srcset”, and “sizes” for Responsive Images

[https://webdesign.tutsplus.com/quick-tip-how-to-use-html5-picture-for-responsive-images--cms-21015t](https://webdesign.tutsplus.com/quick-tip-how-to-use-html5-picture-for-responsive-images--cms-21015t)

</blockquote>

