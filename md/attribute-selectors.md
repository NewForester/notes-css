<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## Attribute Selectors

CSS selectors choose the elements to which a style rule applies, for example, on the basis of class.

Here we are concerned with selecting elements on the basis of their attributes.

This example selects all links with an explicit ``target`` attribute:

```css
    a[target] { background-color: yellow }
```

The next sophistication is selecting on the basis of the  attribute and its value:

```css
    a[target="_blank"] { background-color: yellow }
```

The other selectors have syntax reminiscent of regular expressions:

```css
    [title="xyz"] { ... }               /* elements whose title is "xyz" */
    [title^="xyz"] { ... }              /* elements whose title begins with "xyz" */
    [title$="xyz"] { ... }              /* elements whose title end with "xyz" */
    [title*="xyz"] { ... }              /* elements whose title contains "xyz" */
    [title~="xyz"] { ... }              /* elements whose title contains the word "xyz" */
    [title|="xyz"] { ... }              /* elements whose title begins with the word "xyz" (or "xyz-") */
```

Attribute selectors are useful for styling elements without class or id.
Of particular interest are input forms, which are covered next.

</body>
</html>
