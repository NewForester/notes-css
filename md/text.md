<!DOCTYPE html>
<html>

<meta charset="UTF-8" />
<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Text Properties

An HTML element may have one or more of a number of text properties (over and above its font properties):

  * color               - the colour of the text: [colour name, RGB value, HEX value];
  * text-align          - the horizontal alignment: [left, center, right, justify];
  * text-decoration     - one of [none, overline, line-through, underline];
  * text-transform      - one of [uppercase, lowercase, capitalize];
  * text-indent         - depth of indentation of the first line of text: [px, ...];
  * text-shadow         - horizontal and vertical position (positive means up and right) and colour;
  * test-overflow       - how text that overflows the containing element should be displayed;
  * letter-spacing      - extra space between characters (negative means less): [px ...];
  * word-spacing        - extra space between words (negative means less): [px ...];
  * word-break          - set to `break-all` to allow a word to be broken anywhere, `keep-all` to prevent word break;
  * word-wrap           - set to `break-word` to allow unbreakable words to be broken
  * line-height         - the space between lines: (e.g. 2.0, 0.75);
  * vertical-align      - set the vertical alignment of an element; there are quite a few choices;
  * white-space         - specifies how white-space inside an element is handled;

The default colour for text is that of the `<body>` element.

For proper W3C compliant CSS, the background-color should also be defined whenever the color property is defined.

Note: `text-decoration=none` is used to stop links being underlined.

There are also the properties `unicode-bidi` and `direction` that have something to do with overriding the
text direction in documents that contain quotes in different writing systems.

The `text-overflow` property can take the following values:

  * clip        - clips the text (default)
  * ellipsis    - renders &hellip; to represent clipped text
  * string      - renders the given string to represent clipped text
  * initial     - sets the property to its default value
  * inherit     - sets the property to inherit from the property of the element's parent

</body>
</html>
