<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Text Properties

A HTML element may have one or more of a number of text properties (over and above its font properties):

  * color               - the colour of the text: [colour name, RGB value, HEX value];
  * text-align          - the horizontal alignment: [left, center, right, justify];
  * text-decoration     - one of [none, overline, line-through, underline];
  * text-transform      - one of [uppercase, lowercase, capitalize];
  * text-indent         - depth of indentation of the first line of text: [px, ...];
  * text-shadow         - horizontal and vertical position (positive means up and right) and colour;
  * letter-spacing      - extra space between characters (negative means less): [px ...];
  * word-spacing        - extra space between words (negative means less): [px ...];
  * line-height         - the space between lines: (e.g. 2.0, 0.75);

  * vertical-align      - set the vertical alignment of an element; there are quite a few choices;
  * white-space         - specifies how white-space inside an element is handled;

The default colour for text is that of the `<body>` element.

For proper W3C compliant CSS, the background-color should also be defined whenever the color property is defined.

Note: `text-decoration=none` is used to stop links being underlined.

There are also the properties `unicode-bidi` and `direction` that have something to do with overriding the
text direction in documents that contain quotes in different writing systems.

</body>
</html>
