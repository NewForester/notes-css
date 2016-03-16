<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Tables

A number of CSS properties are commonly used to improve the appearance of HTML tables:

  * table and cell borders;
  * table width and row height;
  * horizontal and vertical alignment;
  * padding and indentation;
  * shading of rows;
  * responsive tables;

<hr /><!-- Tables and Borders -->

The border is typically set with:

```html
    table {
        border-collapse: collapse;
    }

    table, th, td {
       border: 1px solid black;
    }
```

Without the `border-collapse` property, each cell has a border.
This means two borders between each cell.

Horizontal dividers may be created by setting only the `border-bottom` property.

<hr /><!-- Width and Height -->

Typically the table width is set to a percentage of the enclosing block element while row heights are absolute:

```html
    table {
      width: 100%;
    }

    th {
      height: 50px;
    }
```

Column widths may also be specified.

<hr /><!-- Horizontal and Vertical Alignment -->

By default, text in `<th>` elements is centre aligned and in `<td>` elements left aligned.

By default the vertical alignment of both is middle.

<hr /><!-- Padding and Indentation -->

Padding may be used to control the space between cell borders and cell contents.

Text within a cell can be offset (indented) using the `padding-left` property.

<hr /><!-- Striped and Hoverable Tables -->

Alternate rows may be given different backgrounds:

```html
    tr:nth-child(even) {
      background-color: #f4f4f54
    }
```

Table rows may be high-lighted on mouse-over using the `:hover` selector:

```html
    tr:hover {
      background-color: #f4f4f4;
    }
```

<hr /><!-- Responsive Tables -->

A responsive table is one that will display a horizontal scroll bar if the screen is too narrow to display the full text content.

Enclose the table thus:

```html
    <div style="overflow-x:auto;">

    <table>
      ... table content ...
    </table>

    </div>
```

</body>
</html>
