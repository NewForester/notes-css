<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Pagination

This is not about using CSS to turn a long page into several.
It is a about having a row of buttons to navigate between the pages of a web site.

It builds on the previous topic (see [Buttons](buttons.html)) and does not introduce any new properties.

The HTML of the examples is:

```html
    <div class="center">
        <div class="pagination">
            <a href="#">&laquo;</a>
            <a href="#">1</a>
            <a href="#" class="active">2</a>
            <a href="#">3</a>
            <a href="#">4</a>
            <a href="#">5</a>
            <a href="#">6</a>
            <a href="#">&raquo;</a>
        </div>
    </div>
```

Most of CSS is about the definition of the class pagination:

```css
    .pagination {
        display: inline-block;
    }

    .pagination a {
        color: black;
        float: left;
        padding: 8px 16px;
        text-decoration: none;
    }
```

To highlight the button for the current (active) page add something along the lines:

```css
    .pagination a.active {
        background-color: blue;
        color: white;
    }
```

To highlight other buttons on mouse over add something along the lines:

```css
    .pagination a:hover:not(.active) {
        background-color: grey;
    }
```

To make the user want a bigger, faster, browser:

```css
    .pagination a {
        transition: background-color 0.5s
    }
```

You can add borders between the buttons (note no worries about double borders this time) and
round the two at the ends:

```css
    .pagination a {
        border: 1px solid grey;
    }

    .pagination a:first-child {
        border-top-left-radius: 5px;
        border-bottom-left-radius: 5px;
    }

    .pagination a:last-child {
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
    }
```

Use the margin property to put some space between the buttons:

```css
    .pagination a {
        margin: 0 4px;
    }
```

To centre the pagination, centre the container:

```css
    .center {
        text-align: center;
    }
```

<hr />

An alternative is the 'breadcrumbs' approach that implies a hierarchy:

```css
    ul.breadcrumb {
        padding: 8px 16px;
        list-style: none;
        background-color: grey
    }

    ul.breadcrumb li {
        display: inline;
    }

    ul.breadcrumb li+li:before {
        padding: 8px;
        color: black;
        content: "/\00a0";
    }

    ul.breadcrumb li a {
        color: blue;
    }
```

which appears something like:

<style>
    ul.breadcrumb {
        padding: 8px 16px;
        list-style: none;
        background-color: #eee;
    }
    ul.breadcrumb li {display: inline;}
    ul.breadcrumb li+li:before {
        padding: 8px;
        color: black;
        content: "/\00a0";
    }
    ul.breadcrumb li a {color: blue;}
</style>

<ul class="breadcrumb">
    <li><a href="#">World</a></li>
    <li><a href="#">Europe</a></li>
    <li><a href="#">South</a></li>
    <li>Italy</li>
</ul>

</body>
</html>
