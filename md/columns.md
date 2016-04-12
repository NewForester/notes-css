<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Columns

Multi-column layout allow text in several columns just as in newspapers and magazines.

While part of CSS3, browsers are not keen to support it.
Mozilla still uses the -moz- prefix and other major browsers -webkit-:  only IE10 is compliant.
Mozilla does not support column-span but is the only browser to support column-fill.

The column properties are:

  * `column-count`      - the number of columns to divide the element into;
  * `column-fill`       - how to fill columns, one of [balance, auto];
  * `column-gap`        - gap between columns (typically pixels);
  * `column-rule-style` - a line style;
  * `column-rule-width` - typically pixels;
  * `column-rule-color` - any CSS colour;
  * `column-rule`       - shorthand for width, style and colour;
  * `column-span`       - how many columns an element (e.g header) should span (may be `all`);
  * `column-width`      - optimal column width (suggestion only);
  * `column`            - shorthand for width and count;

The treatment of this topic is so short one has to wonder.
It writes about filling columns with text but presumably other elements, such as headers and images, can also be used.

</body>
</html>
