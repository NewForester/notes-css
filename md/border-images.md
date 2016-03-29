<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Border Images

The `border-image` property allows an image to be used for the border around an element.
It has only recently been fully supported.

Note:  the `border-image` property will not work unless the `border` property is set.

The `border-image` property is a shorthand property:

```css
    #borderimg {
      border: 10px solid transparent;
      border-image: url(border.png) 30 round;
    }
```

is equivalent to:

```css
    #borderimg {
      border: 10px solid transparent;
      border-image-source: url(border.png);
      border-image-slice: 30;
      border-image-repeat: round;
    }
```

These three properties are required.
The full set are:

```css
    #borderimg {
      border-image-source:  ...;
      border-image-slice:   ...;
      border-image-width:   ...;
      border-image-outset:  ...;
      border-image-repeat:  ...;
    }
```

<hr /><!-- Border Image Source -->

The `border-image-source` property specifies the image to used to display the border.

It can be expressed as a URL or
take one of the values `none`, `initial` or `inherit`.

When `none`, the border image properties are ignored and the conventional border properties are used instead.


<hr /><!-- Border Image Slice -->

The `border-image-slice` property specifies how to slice the image.
It can be expressed as numbers, percentages or
take one of the values `fill`, `initial` or `inherit`.

The images is always sliced into nine tiles:  four 'corners', four 'edges' and the 'middle'.
The 'middle' tile is treated as fully transparent unless the `fill` keyword is given.

The property consists of potentially three values:  slice in the horizontal, slice in the vertical and fill.

When expressed as numbers, the numbers represent pixels for raster images and co-ordinates for vector images.

When expressed as percentages, they are relative to the width/height of the element's box.

The tutorial makes no attempt to explain how to choose the values and, indeed,
it is not at all obvious why the values given in the examples should produced the effects they do.


<hr /><!-- Border Image Width -->

The `border-image-width` property is the width of the border image.
It can be expressed as a length (e.g. pixels), a number, a percentage or
take one of the values `auto`, `initial` or `inherit`.

When expressed as a number, the property's value is the product of the number and the `border-width` property's value.

When expressed as a percentage, it is relative to the width/height of the element's box.

With `auto`, the property's value is the image's width/height.

As with the conventional border properties, the property may take one to four values.


<hr /><!-- Border Image Outset -->

The `border-image-outset` property is the distance the border image is 'outset' from the conventional border.
It can be expressed as a length (e.g. pixels), a number or
take one of the values `auto`, `initial` or `inherit`.

When expressed as a number, the property's value is the product of the number and the `border-width` property's value.

As with the conventional border properties, the property may take one to four values.


<hr /><!-- Border Image Repeat -->

The `border-image-repeat` property can take the values `round`, `space`, `stretch`, `repeat`, `initial` and `inherit`.

With `stretch` the 'edge' tiles of the image are scaled to fit, resulting in very wide and tall tiles.

With `repeat`, `space` and `round`, the 'edge' tiles are repeated to fill the border width or height.
They differ in how the half tiles adjacent to the corners are filled:

  * `repeat` will use a clipped tile image;
  * `space` will use blank space;
  * `round` will use another whole tile image and then scale the tiles to fit neatly.

<hr />

</body>
</html>
