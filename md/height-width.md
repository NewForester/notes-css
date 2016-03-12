<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Height and Width

The dimensions of an HTML elements are affected by six properties:

  * height and width    - absolute size
  * max_height and max_width    - maximum size
  * min_height and min_width    - minimum size

By default, the values of the `height` and `width` properties is `auto`, which means the browser calculates them.
The min and max forms limit the browser's calculations.

The dimensions are for the element.
They do not include padding, border or margins but refer to the area inside these.

The dimensions may be specified in [px, cm, ...] or as a % of the enclosing element's dimensions.

When absolute dimensions are used, the browser will create scroll bars when the display area is not big enough.
This is particularly noticeable on small screens.

Maximum dimensions override absolute dimensions and lead to fewer scroll bars issues.

</body>
</html>
