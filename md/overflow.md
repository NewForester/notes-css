<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Overflow

The `overflow` property specifies whether to clip content or to add scrollbars when the contents of an element
exceed its width or height.

The overflow property is only relevant when width or height properties are specified
as otherwise the browser calculates the width and/or height such that
the element's box is sufficient to contain its contents.

Text may wrap so vertical overflow may appear to be of more interest but,
with images and more complex content, horizontal overflow may be more important.

The overflow property may take one of four values:

  * visible - overflow is not clipped but is renders outside the element's box (default);
  * hidden - overflow is clipped and the clipped content is invisible;
  * scroll - scrollbars are added so all content may be seen by scrolling;
  * auto - scrollbars area added only when necessary.

With `overflow=scroll` vertical and horizontal scrollbars are added even when not needed.

With `overflow=auto` vertical and horizontal scrollbars are added only as needed.

The `overflow-x` and `overflow-y` properties provide greater control over how overflow is handled.
They do not affect when overflow occurs in either dimension.

</body>
</html>
