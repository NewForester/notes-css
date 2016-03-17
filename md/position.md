<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Position

The position property specifies the method by which an element is positioned.
It is one of:

  * static      - positioned according to the normal flow of the page (default)
  * relative    - positioned relative to the element's static position
  * fixed       - positioned fixed relative to the viewport so it does not move as content is scrolled
  * absolute    - positioned fixed relative to the element's nearest positioned ancestor

An element is positioned if it has a position property other than static.

For positioned properties, four more properties are pertinent:

  * top or bottom
  * left or right

It does not make sense to use both top and bottom or left and right.
Examples show these properties representing pixel offsets.

With `position=relative`, the element is positioned away from its default static position:

```html
    div.relative {
      position: relative
      top: 30px;
      left: 30px;
    }
```

will position the element 30 pixels down and to the right.

With `position=relative`, other content is not moved.
Elements may therefore overlap and a blank space will appear there the static element would appear.

With `position=fixed` or `position=absolute`, no space is reserved for the static element.

With `position=absolute`, ancestor defaults to the `<body>` element.

<hr /><!-- Overlapping elements -->

When elements are positioned they may overlap other elements.
By default, the last overlapping element (encountered in the HTML source) will be shown on top.

Alternatively the `z-index` property can be used to established a 'stack'.
Try `z-index: -1` to place an element underneath another and `z-index: 1` to place an element on top of another.

The following may be used to position text on top of an image:

```html
    .center {
      position: absolute;
      top: 50%;
      left: 0;
      text-align: center;
      width: 100%;
    }

    img {
       opacity: 0.3;
    }

    <div class="container">
      <img ... >
      <div class="center">Centered</div>
    </div>
```

</body>
</html>
