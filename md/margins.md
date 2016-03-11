<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Margins

A HTML element has four margins outside its four borders.
Their properties can be set as one or individually but there is only one.

  * width       - one of [auto, inherit], a specific width in [px, pt, cm, em, ...] or a % of the width of the containing (outside) element

Setting the `margin` property to `auto` will centre the element horizontally within its containing element.

Setting the `margin` property to `inherit` will inherit the property from the containing element.

The bottom margin of one element and the top margin of element below are (sometimes) collapsed:
the margin between the two elements is set to the larger of the two.

<hr /><!-- Shorthand -->

The shorthand `margins` property may be used to set all the margin properties in one statement:

```css
    p {
      margin: 5px;
    }
```

s equivalent to:

```css
    p {
      margin-top: 5px;
      margin-right: 5px;
      margin-bottom: 5px;
      margin-left: 5px;
    }
```

Note that:

  * one value applies to all four margins;
  * a second value applies to the right and left margins;
  * a third value applies to the bottom margin;
  * four values are applied to the top, right, bottom and left margins;

</body>
</html>
