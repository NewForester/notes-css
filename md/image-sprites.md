<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

# Image Sprites Example

An image sprite is a collection of images put into a single image.

Why ?  A web page with a larger number of images generates a larger number of server requests and takes a longer to load.

Imagine a number of icon images used for navigation all packed together into a single image sprite.
The trick to displaying one image from the sprite is to use the sprite as a `background` property and
the `background-position` property to clip all but the unwanted image.

Here are the basics:

```css
    #navlist {
        position: relative;
    }

    #navlist li {
        height: 44px;
        width: 46px;
        display: block;
        }

    #home {
        left: 0px;
        background: url(img_navsprites.gif) 0 0;
    }
```

The `width` and `height` declare the size of the image to be clipped from the sprite
(it will be easier if they are all the same size).
The `background` declares the sprite and where it should be displayed.
The where is relative to the parent HTML list item so the offsets will be negative.

The id `#home`, for example, will display the image from the top left of the sprite.

To declare ids that will display the next two images (in the top row of the sprite):

```css
#prev {
    left: 64px;
    background: url('img_navsprites.gif') -46px 0;
}

#next {
    left: 128px;
    background: url('img_navsprites.gif') -92px 0;
}
```

The `left` property means to the right of the navlist's list element;
the negative offset means move the sprite left under the 44px x 46px display area of the list item and then clip.

To add a hover effect, we need a second row of icons to be displayed as the user mouses over the first row of icons:

```css
    #home a:hover {
        background: url('img_navsprites_hover.gif') 0 -44px;
    }

    #prev a:hover {
        background: url('img_navsprites_hover.gif') -46px -44px;
    }

    #next a:hover {
        background: url('img_navsprites_hover.gif') -92px -44px;
    }
```

The advantage here is that mouse over does not involve a lag while the browser fetches a different image from the server.

Simple really but in practice probably a devil to set up.

</body>
</html>
