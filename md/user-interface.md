<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## User Interface

The tutorial lists the following properties:

  * `box-sizing`      include the padding and border in an element's total width and height
  * `nav-down`        destination of the arrow-down navigation key
  * `nav-index`       the tabbing order for an element
  * `nav-left`        destination of the arrow-left navigation key
  * `nav-right`       destination of the arrow-right navigation key
  * `nav-up`          destination of the arrow-up navigation key
  * `outline-offset`  space between an outline and the edge or border of an element
  * `resize`          whether or not an element is resizable by the user

The `nav-*` properties are currently not implemented by major browsers and are not covered by the tutorial.
I seem to remember from other contexts that navigation order of forms was important.
It is therefore curious that HTML and CSS do so well without.

The `resize` and `outline-offset` properties are not supported by IE.


<hr /><!-- Box Size -->

The (max) height and (max) width properties of an element determine its size but, by default, this size is the area reserved for
the elements contents and does not include padding, border, margins or outline.

The `box-sizing` property allows some redress:

  * `content-box`       the default, minimum definition
  * `border-box`        include content, padding, border but not margins


<hr /><!-- Outline Offset -->

The outline is drawn outside an element's margin, while the border is inside the margin.
See [Outline Property](outline.html).

The outline offset specifies the offset of the outline relative to the margin.
Default is 0.

Apparently an outline does not take up space and need not be rectangular.
The first implies it may be drawn over adjacent elements.
The second is not described any further.


<hr /><!-- Resize Tab -->


The resize tab is a little icon that may appear in the bottom right corner of an element that the user may use to resize the element.

The property takes one of three values that indicate the direction in which the element may be resized:

  * horizontal
  * vertical
  * both

This property is generally used with `overflow: auto` and with the `border` property.

</body>
</html>
