<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Backgrounds

The CSS background properties are used to define the background colour or image for HTML elements.

Use the `<body>` element to set the background for the entire page.

The background colour and image may be set as follows:

```html
    body {
      background-color: colour-value;
    }
```

and

```html
    body {
      background-color: url("image");
    }
```

but there seems little point in using both on the same element.

The 'colour-value' is a name, RGB or HEX colour value;  the 'image' is a valid URL.
Note the required `url(...)` syntax.

When using a background image, several other attributes may be useful.

<hr />

The image will be repeated (aka tiled), not scaled, to cover the entire element.
Use the `background-repeat=` attribute to alter the tiling:

  * repeat-x    - only repeat horizontally
  * repeat-y    - only repeat vertically
  * no-repeat   - only show the background image once

<hr />

The `background-attachment=` property can (and is typically) used to stop the background scrolling with the rest of the element/page.

With `no-repeat` the image will appear in the top left corner by default.
This can be altered using the `background-position=` attribute:

  * right top   - same as top right
  * left        - same as center left
  * bottom      - same as bottom center

but there are other ways to specify the position.

I think `background-position=` should work with other values for `background-repeat=`
but many combinations may appear to have no effect.

<hr /><!-- Shorthand -->

The shorthand `background` property may be used to set several properties in one statement:

```html
    body {
      background: #ffffff url("img_tree.png") no-repeat fixed right top;
    }
```

is equivalent to:

```html
    body {
      background-color: #ffffff;
      background-image: url("img_tree.png");
      background-repeat: no-repeat;
      background-attachment: fixed;
      background-position: right top;
    }
```

'No change' values may be ommitted as along as the value that are given are in the order shown.

</body>
</html>
