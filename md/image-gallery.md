<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## Image Gallery Example

CSS can be used to create an image gallery.
The gallery can be made 'responsive'
in that how many images are displayed side-by-side depends on the width of the display area (aka device screen).

Here is the basic CSS:

```css
    div.gallery {
        margin: 5px;
        border: 1px solid #ccc;
        float: left;
        width: 180px;
    }

    div.gallery:hover {
        border: 1px solid #777;
    }

    div.gallery img {
        width: 100%;
        height: auto;
    }

    div.desc {
        padding: 15px;
        text-align: center;
    }
```

and here is the corresponding HTML for a single image:

```html
    <div class="gallery">
        <a target="_blank" href="forest.jpg">
            <img src="forest.jpg" alt="Fjords" width="300" height="200">
        </a>
        <div class="desc">Add a description of the image here</div>
    </div>
```

The core to making this responsive is covered later.  For now:

```css
    .responsive {
        padding: 0 6px;
        float: left;
        width: 24.99999%;
    }

    @media only screen and (max-width: 700px){
        .responsive {
            width: 49.99999%;
            margin: 6px 0;
        }
    }

    @media only screen and (max-width: 500px){
        .responsive {
            width: 100%;
        }
    }
```

change the `width` property of each image to show 4, then 2 then 1 image for narrower and narrower screens.

This example came without explanation and included:

```css
    * {
        box-sizing: border-box;
    }

    .clearfix:after {
        content: "";
        display: table;
        clear: both;
    }
```

The first means the width and height of elements includes the padding and border (but not the margin).
By default only the contents is included.
The seems to contradict what I had read earlier in the same tutorial

The purpose of the `clearfix` class is unclear but I think it is a kind of 'line break' after the image gallery and
presumably is more effective that placing the image gallery into some container element.

</body>
</html>
