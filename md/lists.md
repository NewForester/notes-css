<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Lists

CSS properties are most often used on lists to:

  * select different list item markers;
  * use an image as a list item marker;
  * add background colours to list and list items;

The `list-style-type` property specifies the item marker to be used:

  * circle
  * square
  * upper-roman
  * lower-alpha

Some are intended for unordered lists and other for ordered lists but may do what you want.
For more details see [CSS list-style-type Property](https://www.w3schools.com/cssref/pr_list-style-type.asp).

To remove the item markers altogether set the style to none:

```html
    ul { list-style-type: none; }
```

The `list-style-image` specifies an image to be used as the item marker:

```html
    ul { list-style-image: url('sqpurple.gif'); }
```

By default, the item marker is placed outside the content flow.
To use the alternative:

```html
    ol { list-style-position: inside; }
```

There is a short-hand property:

```html
    ul { list-style: square inside url("sqpurple.gif"); };
```

that is equivalent to:

```html
    ul {
         list-style-type: square;
         list-style-position: inside;
         list-style-image: url("sqpurple.gif");
    }
```

Default values may be omitted provided those that are specified are in the order shown.

Background colour may be used to illustrate how CSS styles are applied to sub-elements:

```html
    ol {
        background: #ff9999;
        padding: 20px;
    }

    ol li {
        background: #ffe5e5;
        padding: 5px;
        margin-left: 35px;
   }
```

</body>
</html>
