<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Images

There are number of ways images may be styled and responsive effects created with CSS3.
Not all require a script.

<hr /><!-- Rounded Images and Thumbnails -->

Use the `border-radius` property to round the corner of images:

```css
    img {
        border-radius: 8px;
    }

    img {
        border-radius: 50%;
    ]
```

A border radius of 50% will turn a rectangular image into elliptical image.

A thumbnail effect can be achieved using a border and a little padding:

```css
    img {
        border: 1px solid #ddd;
        border-radius: 4px;
        padding: 5px;
    }
```

The thumbnail can be turned into a link by enclosing it in an `<a>` element.
It is nice to change the appearance subtly when the mouse passes over the image:

```css
    img:hover {
        box-shadow: 0 0 2px 1px rgba(0, 140, 186, 0.5);
    }
```

<hr /><!-- Responsive Images -->

Responsive images will automatically adjust to fit different sized screens.

This will scale an image down but not up:

```css
    img {
        height: auto;
        max-width: 100%;
    }
```

To centre an image, make it display as a block element and set the margin to auto:

```css
    img {
        display: block;
        margin: auto;
        width: 50%
    }
```

<hr /><!-- Polaroid Images and Cards -->

You can achieve a Polaroid image effect by using a fading shadow around a container around an image and its description:

```css
    <style>
        div.polaroid {
            width: 80%;
            background-color: white;
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
            margin-bottom: 25px;
        }

        div.description {
           text-align: center;
           padding: 10px 20px;
        }
    </style>

    <div class="polaroid">
        <img src="bla.jpg" alt="bla bla" style="width:100%">
        <div class="description">
            <p>bla bla bla</p>
        </div>
    </div>
```

<hr /><!-- Transparent Images and Image Text -->

An image can be made to appear transparent:

```css
    img {
        opacity: 0.5;
    }
```

Text that is not semi-transparent can be superposed using a sibling element.

```css
    <style>
        .container {
            position: relative;
        }

        .center {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 18px;
        }

        img {
            width: 100%;
            height: auto;
            opacity: 0.3;
        }
    </style>

    <div class="container">
        <img src="bla.jpg" alt="bla bla" width="1000" height="300">
        <div class="center">Centered</div>
    </div>

```

Note:  for the text, the top and left properties have the values 50%.
That puts the top-left corner of the class' element in the middle of the image,
not the text that it contains.
The transform property then moves the text, regardless of its length,
so that the text appears in the middle of the image.

<hr /><!-- Image Filters -->

The CSS `filter` property may be used to add visual effects to an element.
Visual effects are things like blur and saturation.

This is a big enough topic to have its own page:
[CCS Filter Reference](https://www.w3schools.com/cssref/css3_pr_filter.asp).
Note this is a reference, not a tutorial section.

<hr /><!-- Image Hover Overlay -->

When combined with the `hover` selector and the `transition` property an overlay effect can be created:

<style>
    .container {
        position: relative;
        width: 20%;
    }

    .image {
        display: block;
        width: 100%;
        height: auto;
    }

    .overlay {
        position: absolute;
        bottom: 0;
        left: 100%;
        right: 0;
        background-color: #008CBA;
        overflow: hidden;
        width: 0;
        height: 100%;
        transition: .5s ease;
    }

    .container:hover .overlay {
        width: 100%;
        left: 0;
    }

    .text {
        white-space: nowrap;
        color: white;
        font-size: 20px;
        position: absolute;
        overflow: hidden;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>

<div class="container">
    <img src="../images/img_avatar.png" alt="Avatar" class="image">
    <div class="overlay">
        <div class="text">Hello World</div>
    </div>
</div>

<hr /><!-- Responsive Image Gallery -->

When CSS is used to create image galleries, media queries may be used to arrange the images differently on different sized screens.

The essentials are:

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

Here `responsive` is class with different properties for different sized screens.
For progressively smaller screen sizes, the value of the `width` property ensures that 4, 2 and then 1 image appear side-by-size.

There is more in the [CSS RWD Tutorial](https://www.w3schools.com/css/css_rwd_intro.asp).

<hr /><!-- Model Image -->

The final part of the tutorial combines CSS and JavaScript to display a modal window.
The ordinary image is a tad small, the modal window shows it full size.

I need to learn some JavaScript before trying to understand what is really going on.

</body>
</html>
