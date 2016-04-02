<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Shadows

With CSS3, shadows can be added to text and element (boxes) using the attributes:

  * `text-shadow` and
  * `box-shadow`

In their simplest form, these are a (black) shadow with a horizontal and vertical offset:

```css
    text-shadow: 2px 2px;
    box-shadow: 10px 10px;
```

The shadow may be given a colour:

```css
    text-shadow: 2px 2px red;
    box-shadow: 10px 10px grey;
```

It may also have a blurring effect:

```css
    text-shadow: 2px 2px 5px red;
    box-shadow: 10px 10px 5px grey;
```

A 'neon glow' effect is a shadow with a blur but no offset:

```css
    text-shadow: 0 0 3px red;
```

Several shadows are allowed:

```css
    color: white;
    text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
```

<style>
    #halo {
        color: white;
        text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
    }
</style>

<div class="indent">
    <h1 id=halo>Text halo effect !</h1>
</div>

Using four 'shadows' it is possible to outline text:

```css
    color: yellow;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
```

<style>
    #outline {
        color: yellow;
        text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
    }
</style>

<div class="indent">
    <h1 id=outline>Text outline effect !</h1>
</div>

Card effects may be created around element boxes (particularly those containing images)
using more than one shadow and RGBA colours to achieve transparency effects.

</body>
</html>
