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
      background-image: url("image.gif");
    }
```

there mmight seem little point in using both on the same element,
but the browser will fall back to the colour should the image not be found.

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
      background: #ffffff url("image.png") no-repeat fixed right top;
    }
```

is equivalent to:

```html
    body {
      background-color: #ffffff;
      background-image: url("image.png");
      background-repeat: no-repeat;
      background-attachment: fixed;
      background-position: right top;
    }
```

'No change' values may be omitted as along as the value that are given are in the order shown.

<hr />

## CSS3 Backgrounds

CCC3 allows multi-backgrounds and adds three new properties:

  * background-size
  * background-origin
  * background-clip

<hr /><!--Background Size -->

The `background-size` property allows the size of the background image to be specified independently of the image size.

It can be expressed as a length, a percentage or as one of the keywords `contain` or `cover`.

With the `contain` keyword the image is scaled without distortion and without being clipped
to cover as much of the background as possible.

With the `cover` keyword the image is scaled without distortion to cover the entire background and then clipped to fit.

To specify a background image that covers the entire browser window at all times use:

```css
    html {
      background: url(image.png) no-repeat center fixed;
      background-size: cover;
    }
```

<hr /><!--Background Origin and Clip -->

The `background-origin` property gives the area, relative to the element's box,
that should be covered by the background image:

  * border-box  - the background image also covers the box margins;
  * padding-box - the background image covers the box padding but not the margins;
  * content-box - the background image covers the contents area only;

The default is `padding-box`.

The `background-clip` property gives the area relative to the element's box
that should be covered by the background colour.

It does for the background colour what `background-origin` does for the background image.
However, the default is `border-box`.


<hr /><!-- Multiple backgrounds -->

Multiple backgrounds is an 'and', not an 'or'.
Each background has its own properties.
The properties are now comma separated lists:

```css
    background-image: url(image.gif), url(wallpaper.gif);
    background-position: right bottom, left top;
    background-repeat: no-repeat, repeat;
```

and the same for the shorthand background property:

```css
    background: url(image.gif) right bottom no-repeat, url(wallpaper.gif) left top
```

The first background covers the second, covers the third ...

<hr />

</body>
</html>
