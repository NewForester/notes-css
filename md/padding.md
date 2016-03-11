<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Padding

A HTML element has padding inside its four borders.
Padding properties can be set for all four sides or individually but there is only one.

  * width       - one of [inherit], a specific width in [px, pt, cm, em, ...] or a % of the width of the (inside) element

Setting the `padding` property to `inherit` will inherit the property from the containing element.

<hr /><!-- Shorthand -->

The shorthand `padding` property sets the width/height of the padding on all four sides at once:

```css
    p {
      padding: 5px;
    }
```

is equivalent to:

```css
    p {
      padding-top: 5px;
      padding-right: 5px;
      padding-bottom: 5px;
      padding-left: 5px;
    }
```

Note that:

  * one value applies to all four sides;
  * a second value applies to the right and left sides;
  * a third value applies to the bottom;
  * four values are applied to the top, right, bottom and left sides;

</body>
</html>
