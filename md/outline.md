<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Outline

A HTML element may have an outline.
The outline may be thought of as a border outside of the element margin
while the border proper is inside the margin.

The properties of the outline can only be set for all four sides
but the most common of the properties are the same as for the border property:

  * style       - one of [dotted, dashed, solid, double, groove, ridge, insert, outset, none, hidden]
  * width       - one of [thin, medium, thick] or a specific width in [px, pt, cm, em, ...]
  * color       - a colour name, RGB value or HEX value or invert.

Since the default style is none, the width and colour properties have no effect unless style is set.

The width is not part of any element's total width:  the outline is superimposed.

Use `color=invert` sets the colour to the inverse of whatever the outline lies upon.
Use this to ensure the outline is always visible.

<hr /><!-- Shorthand -->

The shorthand `outline` property may be used to set several properties in one statement:

```css
    p {
      outline: 5px solid red;
    }
```

is equivalent to:

```css
    p {
      outline-width: 5px;
      outline-style: solid;
      outline-color: red;
    }
```

'No change' values may be ommitted as along as the values that are given are in the order shown.

<hr />

The `outline-offset` specifies the space between the outline and the outer edge of the element.

```css
    p {
      outline-offset: 5px;
    }
```

</body>
</html>
