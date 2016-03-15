<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Links

Any CSS property may be used to style HTML hyper-links.

Hyper-links have state and different styles may be used for each state.
For example, to change the colour of a link to indicate that it has been visited before.

The four link states are:

  *  a:link     - a normal, unvisited link
  *  a:visited  - a link the user has visited
  *  a:hover    - a link when the user mouses over it
  *  a:active   - a link the moment it is clicked

The properties for the individual states must declared in the order above.

The text decoration property may be used to remove the underlines from links.

```html
    a:link {
    }

    a:hover {
       background-color: lightgreen;
    }

    a:active {
        background-color: hotpink;
    }

    a:visited {
        text-decoration: none;
    }
```

</body>
</html>
