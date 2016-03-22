<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## Navigation Bar Examples

Most web pages have some means of navigating to related web pages.
Navigation bars are a very common solution.

These are implemented around lists of hyper-link and do not involve and new elements, attributes or properties and values.

Consider first the list:

```html
    <ul>
      <li><a href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
```

The basis of any navigation bar is the list without the bullets and other default styling:

```css
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }
```

will appear as:

<style>
    ul.vex1 {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }
</style>

<div class=indent>
    <ul class="vex1">
      <li><a href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
</div>

### Vertical Navigation Bar

To build a vertical list, style the `<a>` element to display as block element and give then a fixed width:

```css
    li a {
        display: block;         /* make link area, not just link text, clickable */
        width: 80px;            /* otherwise block display will use the available width in full */
    }
```

<hr />

Now add a background that changes colour when the user moves the mouse over it but
mark the active page in a different colour so the user knows which page they are on.

```css
    /* List with no bullets but boxed with a background colour instead */
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 200px;
        background-color: lightgray;
    }

    /* Mark out clickable menu items one to a line */
    li a {
        display: block;
        color: black;
        padding: 8px 16px;
        text-decoration: none;
    }

    /* Change the link colour on hover */
    li a:hover:not(.active) {
        background-color: darkgray;
        color: white;
    }

    /* Different background for the active menu item */
    li a.active {
        background-color: green;
        color: white;
    }
```

will appear as:

<style>
    ul.vex2 {
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 200px;
        background-color: lightgray;
    }

    .vex2 li a {
        display: block;
        color: black;
        padding: 8px 16px;
        text-decoration: none;
    }

    .vex2 li a:hover:not(.active) {
        background-color: darkgray;
        color: white;
    }

    .vex2 .active {
        background-color: green;
        color: white;
    }
</style>

<div class=indent>
    <ul class="vex2">
      <li><a class="active" href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
</div>

<hr />

Next centre the menu item text and put a border around each one and fixed the menu so that it does not scroll.

```css
    /* List with no bullets but boxed with borders and a background colour */
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 200px;
        background-color: lightgray;
        border: 1px solid darkgray;
    }

    /* Centre menu items within borders */

    li {
        text-align: center;
        border-bottom: 1px solid darkgray;
    }

    /* Mark out clickable menu items one to a line */
    li a {
        display: block;
        color: black;
        padding: 8px 16px;
        text-decoration: none;
    }

    /* Change the link colour on hover */
    li a:hover:not(.active) {
        background-color: darkgray;
        color: white;
    }

    /* Different background for the active menu item */
    li a.active {
        background-color: green;
        color: white;
    }
```

will appear as:

<style>
    ul.vex3 {
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 200px;
        background-color: lightgray;
        border: 1px solid black;
    }

    .vex3 li {
        text-align: center;
        border-bottom: 1px solid black;
    }

    .vex3 li a {
        display: block;
        color: black;
        padding: 8px 16px;
        text-decoration: none;
    }

    .vex3 li a:hover:not(.active) {
        background-color: darkgray;
        color: white;
    }

    .vex3 li a.active {
        background-color: green;
        color: white;
    }
</style>

<div class=indent>
    <ul class="vex3">
      <li><a class="active" href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
</div>

<hr />

Finally you might want to make the menu full height and fixed so that it does not scroll with the rest of the page:

```css
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 25%;
        background-color: #f1f1f1;
        height: 100%;                     /* Full height */
        position: fixed;                  /* Make it stick, even on scroll */
        overflow: auto;                   /* Enable scrolling if the sidenav has too much content */
    }
```

<hr />

### Horizontal Navigation Bar

Horizontal navigation bars may be created using either inline or floating list items.

Using `display:inline` will stop the browser adding new lines either side of an element
so this can be used to display list items side-by-side.

```css
    li {
        display: inline;
    }
```

will appear as:

<style>
    ul.hex1 {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }

    .hex1 li {
        display: inline;
    }
</style>

<div class=indent>
    <ul class="hex1">
      <li><a href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
</div>

<hr />

Using `float: left` will display block items side-by-side so can be used to achieve a similar effect:

```css
    li {
        float: left;
    }

    a {
        display: block;
        padding: 8px;
        background-color: lightgray;
    }
```

will appear as:

<style>
    ul.hex2 {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }

    .hex2 li {
        float: left;
    }

    .hex2 a {
        display: block;
        padding: 8px;
        background-color: lightgray;
    }
</style>

<div class=indent>
    <ul class="hex2">
      <li><a href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li><a href="about.asp">About</a></li>
    </ul>
</div>

&nbsp;

&nbsp;

<hr />

Here is an example horizontal navigation bar with a dark background that changes colour when
the user moves the mouse over individual items.
The 'active' or current navigation link has a different background colour and
the last item floats at the right hand side of the navigation bar.
The menu item edges are highlighted.

```css
    /* List with no bullets but boxed with a background colour instead */
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
        background-color: darkgray;
    }

    /* Horizontal list with floating items */
    li {
        float: left;
    }

    /* Add a right border to all list items, except the last item (last-child) */
    li {
        border-right: 1px solid white;
    }

    li:last-child {
        border-right: none;
        border-left: 1px solid white;
    }

    /* Mark out clickable menu items one to a line */
    li a {
        display: block;
        color: white;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
    }

    /* Change the link colour on hover */
    li a:hover:not(.active) {
        background-color: lightgray;
    }

    /* Different background for the active menu item */
    li .active {
        background-color: green;
    }
```

will appear as:

<style>
    ul.hex3 {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
        background-color: darkgray;
    }

    .hex3 li {
        float: left;
    }

    .hex3 li {
        border-right: 1px solid white;
    }

    .hex3 li:last-child {
        border-right: none;
        border-left: 1px solid white;
    }

    .hex3 li a {
        display: block;
        color: white;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
    }

    .hex3 li a:hover:not(.active) {
        color : black;
        background-color: lightgray;
    }

    .hex3 li .active {
        background-color: green;
    }
</style>

<div class=indent>
    <ul class="hex3">
      <li><a class="active" href="default.asp">Home</a></li>
      <li><a href="news.asp">News</a></li>
      <li><a href="contact.asp">Contact</a></li>
      <li style="float:right"><a href="about.asp">About</a></li>
    </ul>
</div>

<hr />

Complexities abound:  further changes are necessary to make the navigation bars responsive or to add drop-down menus to navigation bars.


</body>
</html>
