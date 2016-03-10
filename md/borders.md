<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Borders

A HTML element has four borders whose properties can be set as one or individually.
The most common properties are:

  * style       - one of [dotted, dashed, solid, double, groove, ridge, insert, outset, none, hidden]
  * width       - one of [thin, medium, thick] or a specific width in [px, pt, cm, em, ...]
  * color       - a colour name, RGB value or HEX value

These can be set as one or individually.
Since the default style is none, the width and colour properties have no effect unless style is set.

<hr /><!-- Shorthand -->

The shorthand `border` property may be used to set several properties in one statement:

```css
    p {
      border: 5px solid red;
    }
```

is equivalent to:

```css
    p {
      border-width: 5px;
      border-style: solid;
      border-color: red;
    }
```

'No change' values may be ommitted as along as the value that are given are in the order shown.

The `border-width`, `border-style` and `border-color` properties are themselve shorthand properties
that set a property for all four margines in one statement:

```css
    p {
      border-color: red;
    }
```

and is equivalent to:

```css
    p {
      border-top-color: red;
      border-right-color: red;
      border-bottom-color: red;
      border-left-color: red;
    }
```

Note that:

  * one value applies to all four borders;
  * a second value applies to the right and left borders;
  * a third value applies to the bottom border;
  * four values are applied to the top, right, bottom and left borders;

<hr />

The `border-radius` property may be used a round the corners where borders meet:

```css
    p {
      border-radius: 5px;
    }
```

The larger the radius, the more pronounced the rounding.

</body>
</html>
