class 3 reads

# https://learn.shayhowe.com/advanced-html-css/responsive-web-design/

responsive web design focuses on how to build websites suitable for all users. and works on every device and every screen size.  

its all about making design that dynamically adapts to different browsers and device viewports, changing layout and content along the way.

3 main componenets:

1. flexible layouts- a flexible grid that dynamically resizes to any width.  Built using relative length units, % or em, which are then used to declare common grid property values like width, margin and padding.

new viewport measurements in vw, vh, vmin and vmax are designed for responsiveness.

fixed values like pixels have too many constraints and limits for dynamic design, so to help in identifying the proportions of a flexible layout, use this formula for restablishing relative values to use:
    target / context = result

1. media queries-Media queries provide the ability to specify different styles for individual browser and device circumstances.

mobile first is a good rule of thumb, most users view media on mobile screens and this allows for lower bandwidth ad you can build up on them for larger screens.

1. flexible media- setting media to max width property ensures media types will be scalable, changing their size as the size of the viewport changes.  to do this set the max-width property to a value of 100%.

## https://css-tricks.com/all-about-floats/

floated elements allow text to flow around them rather than over them and keep the image within the flow of the webpage.

use the clear property to ensure the media stays beneath two columns for example.  it will clear out of the way of other elements.

### https://css-tricks.com/dont-overthink-it-grids/

steps for setting up a css grid

#### http://smacss.com/book/

css book

