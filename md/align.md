<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Layout - Horizontal and Vertical Alignment

There seems to be no CSS element whose purpose is to align the contents of an element horizontally or vertically within an element.

Instead, there are a number of increasingly sophisticated hacks and workarounds.

<hr /><!-- Horizontal Alignment -->

The horizontal alignment of text within an block element is straight forward.
Use the `text-align` property with one of the values `left`, `center` or `right`.

To centre a block element within its container use `margin: auto`.
This has no effect unless the width property is set.

To centre an image use `margin: auto` and also `display: block` because otherwise the image is displayed as an in-line element.

To align to the right or the left, you can use `position: absolute` with the right or left property.
However, this can lead of elements overlapping.

The alternative is to use the `float` property with the value `right` or `left`.

In either case, for the sake of your own sanity, declare the `margin` and `padding` properties for the `<body>` element.
A value of 0 will do.

<hr /><!-- Vertical Alignment -->

The most common case of vertical alignment seems to be centring text vertically with a larger container.

The cheep and cheerful approach is the padding property.
Calibrating this may be tricky if the text wraps onto more than one line.

An alternative that works for text that wraps onto more than one line is to use a `line-height` property with
the same value as the `height` property:

```css
    .center {
      line-height: 200px;
      height: 200px;
      border: 3px solid green;
      text-align: center;
    }

    /* If the text has multiple lines, add the following: */
    .center p {
      line-height: 1.5;
      display: inline-block;
      vertical-align: middle;
    }
```

This only works if the text is in one paragraph.

For text in more than one paragraph, use:

```css
    .center {
      height: 200px;
      position: relative;
      border: 3px solid green;
    }

    .center p {
      margin: 0;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
```

</body>
</html>
