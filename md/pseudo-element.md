<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Pseudo Elements

CSS pseudo elements may be used to style specific parts of an element's content.

The syntax for pseudo element is:

```css
    selector::pseudo-element { property:value; ... }
```

Note that any selector can be combined with a pseudo element.

<hr /><!-- First Line and First Letter Pseudo Elements -->

The `::first-line` and `::first-letter` pseudo elements may be used to add a special style to the first line
or just the first letter of the displayed text content of an element.

There are about a dozen properties can be used with these pseudo elements and they can be combined:

```css
    p::first-letter {
      color: #ff0000;
      font-size: xx-large;
    }

    p::first-line {
      color: #0000ff;
      font-variant: small-caps;
    }
```

<hr /><!-- Before and After Pseudo Elements -->

The `::before` and `::after` pseudo elements may be used to insert content before or after the content of an element.

```css
    h1::before, h1::after {
      content: url(smiley.gif);
    }
```

<hr /><!-- The Selection Pseudo Element -->

The `::selection` pseudo element matches the portion of an element that is selected by the user.
It is intended for highlighting.

The properties that can be used with this pseudo element are `color`, `background`, `cursor` and `outline`.

```css
    ::selection {
      color: red;
      background: yellow;
    }
```

</body>
</html>
