<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Colours

There are four ways colours may be specified:

  * by name             - eg: `"red"`
  * by RGB value        - eg: `"rgb(255,0,0)"`
  * by HEX value        - eg: `"#ff0000"`
  * by HSL value        - eg: `"hsl(0,100%,50%)"`

Colour names are case insensitive as are hex values.
CSS and HTML support 140 named colours.

RGB and HEX are 24-bit values giving a very large number of shades.

An RGB value gives a figure between 0 and 255 for each of the three primary colours red, green and blue.

No colour is 0, full colour is 255.

This gives rgb(0,0,0) for black and rgb(255,255,255) for white.

Shades of grey have the same value for all three colours.

A hex value is similar to RGB: #RRGGBB with the colour values falling the range 0 to ff.

An HSL colour has values for hue, saturation and lightness:

  * 0 (or 360), 120, 240 are, respectively red, green and blue
  * saturation ranges from grey (0%) to full colour (100%)
  * lightness ranges from black (0%) to white (100%)

The CCS3 `opacity` property has already been discussed in the context of images.
It affects background and foreground colours giving both a washed-out look.

CSS3 introduces a way to specify opacity with a colour that affects just the background or text colour.

  * by RGBA value        - eg: `"rgba(255,0,0,1.0)"`
  * by HSLA value        - eg: `"hsla(0,100%,50%,1.0)"`

The fourth value, with the letter A for alpha channel,
is the opacity ranging from totally transparent (0.0) to totally opaque (1.0).

</body>
</html>
