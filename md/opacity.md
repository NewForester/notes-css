<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Opacity

The `opacity` property specifies the opacity/transparency of an element (not just its background).

The property takes a value in the range 0.0 to 1.0.
The lower the value, the more transparent the element.

```css
    img {
       opacity: 0.5;
       filter: alpha(opacity=50);       /* For IE8 and earlier */
    }
```

The property is often used with the `:hover` pseudo class to highlight the element:

```css
    img         { opacity: 0.5; }
    img:hover   { opacity: 1.0; }

```

When the `opacity` property is used it is not just the background that becomes somewhat transparent bit all its child elements too.
This can make reading text difficult.

The workaround for this when the background is just a colour is to use the RGBA colour and specify the
opacity with the colour:

```css
    div {
      background: rgba(76, 175, 80, 0.3)        /* Green background with 30% opacity */
    }
```

The partial workaround for this when the background is an image is to use bold text:

```css
    div.background {
      background: url(klematis.jpg) repeat;
      border: 2px solid black;
    }

    div.transbox {
      margin: 30px;
      background-color: #ffffff;
      border: 1px solid black;
      opacity: 0.6;
    }

    div.transbox p {
      margin: 5%;
      font-weight: bold;
      color: #000000;
    }
```

</body>
</html>
