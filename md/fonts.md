<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Font Properties

A HTML element has several font properties that affect any text content:

  * font-family:        - font families are serif, sans-serif and monospace;
  * font-size:          - either absolute (px) or relative (em);
  * font-style:         - one of [normal, italic, oblique];
  * font-variant:       - one of [normal, small-caps];
  * font-weight:        - one of [normal, bold];

It may be hard to distinguish oblique text from italic text.

<hr /><!-- Font Family -->

The font family is a comma separated list of font names (from the same font family) terminated by the family name.
The list is a fall-back system:  the first font in the list is preferred but if it is not available,
the next is considered and so on:

```html
    p { font-family: "Times New Roman", Times, serif; }
```

There is a default font for each family but it is system dependent.
There are recommended combinations but they do not look cross-platform.

There are (Google) fonts on-line that are downloaded on the fly.

<hr /><!-- Font Size -->

The font size is absolute if specified in pixels.
This is viewed as bad for accessibility as the user cannot change the text size.

The font size is relative if specified in ems.
This is relative to surrounding elements.
The user can change the text size should they find it too small to read comfortably.

A text size of 1em is equal to the current font size.
For the sake of some older IE browser, set:

```html
    body { font-size: 100%; }
```

The font size may be doubled up with the line height property as shown below.

<hr /><!-- Shorthand -->

The shorthand `font` property may be used to set several properties in one statement:

```html
    p { font:italic normal bold 12px/30px Georgia, serif; }

```

is equivalent to:

```html
    p {
      font-style:     italic;
      font-variant:   normal;
      font-weight:    bold;
      font-size:      12px/30px;
      font-family:    Georgia, serif;
    }
```

'No change' values may be ommitted as along as the values that are given are in the order shown.

</body>
</html>
