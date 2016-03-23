<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## Tool-Tips Example

A tool-tip appears when the user moves the mouse pointer over an element.
It typically provide extra information.

Tool-tips are implemented as simple drop-downs with extra positioning information and sometimes a 'caret'.
Note that the examples here use the `visibility` property rather than the `display` property.

<hr />

Here is the CSS for a basic tool-tip example:

```css
    /* Tool-tip container */
    .tooltip {
        position: relative;
        display: inline-block;
        border-bottom: 1px dotted black;        /* If you want dots under the hoverable text */
    }

    /* Tool-tip text */
    .tooltip .tooltiptext {
        visibility: hidden;
        width: 120px;
        background-color: black;
        color: white;
        text-align: center;
        padding: 5px 0;
        border-radius: 6px;

        /* Position the tool-tip text - not very good (see examples below) */
        position: absolute;
        z-index: 1;
    }

    /* Show the tool-tip text when you mouse over the tool-tip container */
    .tooltip:hover .tooltiptext {
        visibility: visible;
    }
```

and here is the HTML:

```html
    <div class="tooltip">Hover over me ...
        <span class="tooltiptext">Tooltip text</span>
    </div>
```

will appear as:

<style>
    .tooltip {
        position: relative;
        display: inline-block;
        border-bottom: 1px dotted black;
    }

    .tooltip .tooltiptext {
        visibility: hidden;
        width: 120px;
        background-color: black;
        color: white;
        text-align: center;
        padding: 5px 0;
        border-radius: 6px;

        /* Position the tool-tip text - not very good (see examples below) */
        position: absolute;
        z-index: 1;
    }

    .tooltip:hover .tooltiptext {
        visibility: visible;
    }
</style>

<div class="indent ex1">
    <div class="tooltip">Hover over me
        <span class="tooltiptext">Tooltip text</span>
    </div>
</div>

<hr />

Positioning to tool-tip text relies on the use of `display=relative` in the container and
`display=absolute` for the tool-tip.
The results may appear counter-intuitive because the point of reference may not be what you expect.

To place the tool-tip to the left of the container:

```css
    .tooltip .tooltiptext {
        top: -5px;      /* negative of whatever padding is used for the container */
        left: 105%;     /* all the way to the left and then some so there is a gap */
    };
```

To place the tool-tip over the container:

```css
    .tooltip .tooltiptext {
        width: 120px;
        margin-left: -60px;     /* Use half of the width to centre the tool-tip */
        bottom: 100%;
        left: 50%;              /* In conjunction with the margin-left
}
```

<hr />

The caret is created as follows.
Imagine a tidy box, say 5px, with a solid border also 5px.
It would be a little solid box.
It the border is only one side, the quarter that is filled in looks like a little pyramid.

Position it correctly and you have the appearance of a caret attached to the tool-tip.

<style>
    .ex2 .tooltip .tooltiptext::after {
        content: " ";
        position: absolute;
        bottom: 100%;   /* At the top of the tooltip */
        left: 50%;
        margin-left: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: transparent transparent black transparent;
    }
</style>

<div class="indent ex1 ex2">
    <div class="tooltip">Hover over me
        <span class="tooltiptext">Tooltip text</span>
    </div>
</div>

For a caret on the bottom of a tool-tip:

```css
    .tooltip .tooltiptext::after {
        content: " ";
        position: absolute;
        top: 100%;      /* At the bottom of the tooltip */
        left: 50%;
        margin-left: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: black transparent transparent transparent;
    }
```

For a caret on the top of a tool-tip change this so that:

```css
        bottom: 100%;   /* At the top of the tooltip */
        left: 50%;
        border-color: transparent transparent black transparent;
```

For a caret on the left:

```css
        top: 50%;
        right: 100%;    /* To the left of the tooltip */
        border-color: transparent black transparent transparent;
```

For a caret on the right:

```css
        top: 50%;
        left: 100%;     /* To the right of the tooltip */
        border-color: transparent transparent transparent black;

```

<hr />

A combination of the CSS3 transition and opacity properties can be used to give a tool-tip to appearance of fading in.

```css
    .tooltip .tooltiptext {
        opacity: 0;
        transition: opacity 1s;
    }

    .tooltip:hover .tooltiptext {
        opacity: 1;
    }
```

</body>
</html>
