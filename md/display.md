<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Display

The display property is an an important property for controlling output.

HTML elements are either block or span and their default display property values are `block` and `inline` respectively.
The latter can be overridden.

An example of overriding the display property for a block element would be:

```html
    li {
      display: inline;
    }
```

This would list items across, rather than down, the page.
It is often used to create menu bars.

An example of overriding property for a span element would be:

```html
    a {
      display: block;
    }
```

This would display links down, rather than across, the page.
This has the effect of creating a list of links to chose from.

<hr /><!-- Hiding elements -->

An element can be 'removed' from the display by setting its `display` property to `none`.
This is used in scripts to hide and reveal elements rather than delete and re-create them.

```html
    #peek-a-boo {
      display: none;
    }
```

An alternative is the `visibility` property.
When set to `hidden`, an element is not displayed but the space it occupies remains reserved.

```html
    #big-empty-space {
      visibility: hidden;
    }
```

</body>
</html>
