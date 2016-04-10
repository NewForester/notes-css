<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Buttons

Buttons are essential to web pages.
They support hyper-link navigation and data entry on forms.

```css
    <!-- Hyperlink -->
    <a href=# class="button">Link Button</a>

    <!-- Button Elements -->
    <button class="button">Button</button>

    <!-- Input Elements -->
    <input type="button" class="button" value="Input Button">
```

How they appear and behave is largely down to how CSS is used to style the buttons.
This section does not introduce new properties.
It illustrates how properties may be used with buttons.

<hr /><!-- Basic Button Styling -->

The basic button is ugly and a give away.
To override it, consider using some or all of these properties:

```css
    .button {
        background-color:       blue;
        border:                 none;
        color:                  white;
        padding:                15px 32px;
        text-align:             center;
        text-decoration:        none;
        display:                inline-block;
        font-size:              16px;
    }
```

The change the buttons colour use the `background-color` property.

To change the size of the text within the button, use the `font-size` property.

To change the overall size of the button, use the `padding` property.

To round the corners of the button, use the `border-radius` property.

An alternative to the coloured button, is a white button with a coloured border.

<hr /><!-- Changing Button Appearance on Mouse Over -->

It is common to highlight a button as the mouse moves over it.
There are many ways to do this.

This example swaps between a coloured button with no border to a white button with a coloured border:

```css
    .button {
        background-color: green;
        color: white;
        border: none;
        transition-duration: 0.4s;
    }

    .button:hover {
        background-color: white;
        color: black;
        border: 2px solid green;
    }
```

A fading shadow is another form of highlighting:

```css
    .button1 {
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    }

    .button2:hover {
        box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
    }
```

When a mouse crosses a button the cursor changes to a hand (the `cursor: pointer`).
A button that has been disabled might be highlighted thus:

```css
    .disabled {
        opacity: 0.6;
        cursor: not-allowed;
    }
```

By default, the width of a button is determined by the width of the text content (plus padding etc.).
The `width` property may be used to make the button wider.
Use a percentage to specify a fraction of the width of the containing element (often the page/screen).

```css
    .button1 {width: 250px;}
    .button2 {width: 50%;}
    .button3 {width: 100%;}
```

<hr /><!-- Button Groups -->

To place several buttons side-by-side, remove the margin and let them float to the left.

```css
    .button {
        margin: none;
        float: left;
    }
```

Take care to turn the float off for the element that follows:

```css
    <p style="clear:both"><br>Thus.</p>
```

The border property can be used to create a bordered button group:

```css
    .button {
        float: left;
        border: 1px solid green;
    }

    .btn-group .button:not(:last-child) {
        border-right: none;
    }
```

Suppressing the right-hand border prevents a double border appearing between buttons but it does not scale down so well.

To group buttons vertically

```css
    .button {
        display: block;
        border: 1px solid green;
    }

    .btn-group .button:not(:last-child) {
        border-bottom: none;
    }
}

```

<hr /><!-- Animated Buttons -->

CSS animations can be used to good effect.

This example add "»" on mouse over:

```css
    .button { ... }

    .button span {
        position: relative;
        transition: 0.5s;
    }
    .button span:after {
        content: '\00bb';
        opacity: 0;
        position: absolute;
        transition: 0.5s;
    }
    .button:hover span {
        padding-right: 25px;
    }
    .button:hover span:after {
        opacity: 1;
    }
```

This example gives a "pressed" effect on click:

```css
    .button {
        background-color: green;
        box-shadow: 0 9px #999;
    }

    .button:hover {
        background-color: darkgreen;
    }

    .button:active {
        background-color: darkgreen;
        box-shadow: 0 5px #666;
        transform: translateY(4px);
    }
```

This example has a "ripple" effect on click:

```css
    .button {
        position: relative;
        background-color: green;
    }

    .button:after {
        content: "";
        background: #f1f1f1;
        display: block;
        position: absolute;
        padding-top: 300%;
        padding-left: 350%;
        margin-left: -20px !important;
        margin-top: -120%;
        opacity: 0;
        transition: all 0.8s
    }

    .button:active:after {
        padding: 0;
        margin: 0;
        opacity: 1;
        transition: 0s
    }

```

</body>
</html>
