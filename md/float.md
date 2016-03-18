<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Float and Clear

The `float` and `clear` properties determine whether and how elements float.

It is still common to do entire web layouts using these properties.

The simple use the float property is to wrap text around images:

```css
    img {
      float: right;
      margin: 0 0 10px 10px;
    }
```

might be used to float an image to the right of text.

Used just like this, elements declared before and after the floating element may wrap around it.

The clear property may be used to stop this:

```css
    div {
      clear: left;
    }
```

would prevent any element floating to the left of a `<div>` element.

Think of it as a line break before or after a floating element.

<hr /><!-- The clearfix Hack -->

If an element is floated and it is taller than the element containing it, then it will overflow the container.

This can be stopped with:

```css
    .clearfix {
      overflow: auto;
    }
```

This fix works well provided margins and padding are under control but can lead to the appearance of scroll bars.

The new, modern, clearfix hack is safer:

```css
    .clearfix::after {
      content: "";
      clear: both;
      display: table;
    }
```

<hr /><!-- Inline block -->

The `float` property can be used to create a grid of boxes that fills the browser width and
wraps nicely when the browser is resized.
All you need it the `clear` property on whatever comes after the last of the boxes.

An even more convenient way of doing this is with the `display: inline-block` property.
An `inline-block` is an in-line element that can have a width and a height.

Instead of:

```css
    .floating-box {
      float: left;
      ...
    }

    .after-box {
      clear: left;
    }
```

you need just:

```css
    .floating-box {
      display: inline-block;
      ...
    }
```

</body>
</html>
