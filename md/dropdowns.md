<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## Drop-down Examples


Many web pages have a drop-down of some sort.
Drop-down menus are the most common form.

Drop-downs are implemented by changing the value of the `display` property of hidden content in response
to the user moving the mouse pointer over the visible content.

<hr />

Here is the CSS for a basic 'tool-tip' style drop-down example:

```css
    /* Class for the drop-down container */
    .dropdown {
        position: relative;             /* needed so the drop-down content does not push other elements aside */
        display: inline-block;
    }

    /* Class for the drop-down content */
    .dropdown-content {
        display: none;                  /* hidden until mouse over */
        position: absolute;             /* to the content appears just below the container */
        background-color: #f9f9f9;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        padding: 12px 16px;
        z-index: 1;                     /* so the contents appears on top of other elements */
    }

    /* Make the content appear when the mouse is over the container */
    .dropdown:hover .dropdown-content {
        display: block;
    }
```

and here is the HTML:

```html
    <div class="dropdown">
        <span>Mouse over me</span>
        <div class="dropdown-content">
            <p>Hello World!</p>
        </div>
    </div>
```

that will appear as:

<style>
    .ex1 .dropdown {
        position: relative;
        display: inline-block;
    }

    .ex1 .dropdown-content {
        display: none;
        position: absolute;
        background-color: gray;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        padding: 12px 16px;
        z-index: 1;
    }

    .ex1 .dropdown:hover .dropdown-content {
        display: block;
    }
</style>

<div class="indent ex1">
    <div class="dropdown">
        <span>Mouse over me</span>
        <div class="dropdown-content">
            <p>Hello World!</p>
        </div>
    </div>
</div>

<hr />

Here is the CSS for a drop-down menu example:

```css
    /* Style The Dropdown Button */
    .dropbtn {
        background-color: green;
        color: white;
        padding: 16px;
        font-size: 16px;
        border: none;
        cursor: pointer;
    }

    /* The container <div> - needed to position the dropdown content */
    .dropdown {
        position: relative;
        display: inline-block;
    }

    /* Dropdown Content (Hidden by Default) */
    .dropdown-content {
        display: none;
        position: absolute;
        background-color: lightgray;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
    }

    /* Links inside the dropdown */
    .dropdown-content a {
        color: black;
        padding: 12px 16px;
        text-decoration: none;
        display: block;
    }

    /* Change color of dropdown links on hover */
    .dropdown-content a:hover {
        background-color: gray;
    }

    /* Show the dropdown menu on hover */
    .dropdown:hover .dropdown-content {
        display: block;
    }

    /* Change the background color of the drop-down button when the drop-down content is shown */
    .dropdown:hover .dropbtn {
        background-color: darkgreen;
    }
```

and here is the HTML:

```html
    <div class="dropdown">
        <button class="dropbtn">Dropdown</button>
        <div class="dropdown-content">
            <a href="#">Link 1</a>
            <a href="#">Link 2</a>
            <a href="#">Link 3</a>
        </div>
    </div>
```

that will appear as:

<style>
    .ex2 .dropbtn {
        background-color: green;
        color: white;
        padding: 16px;
        font-size: 16px;
        border: none;
        cursor: pointer;
    }

    .ex2 .dropdown {
        position: relative;
        display: inline-block;
    }

    .ex2 .dropdown-content {
        display: none;
        position: absolute;
        background-color: lightgray;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
    }

    .ex2 .dropdown-content a {
        color: black;
        padding: 12px 16px;
        text-decoration: none;
        display: block;
    }

    .ex2 .dropdown-content a:hover {
        background-color: gray;
    }

    .ex2 .dropdown:hover .dropdown-content {
        display: block;
    }

    .ex2 .dropdown:hover .dropbtn {
        background-color: darkgreen;
    }
</style>

<div class="indent ex2">
    <div class="dropdown">
        <button class="dropbtn">Dropdown</button>
        <div class="dropdown-content">
            <a href="#">Link 1</a>
            <a href="#">Link 2</a>
            <a href="#">Link 3</a>
        </div>
    </div>
</div>

<hr />

</body>
</html>
