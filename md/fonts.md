<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Font Properties

A HTML element has several font properties that affect any text content:

  * font-family:        - font families are serif, sans-serif and mono-space;
  * font-size:          - either absolute (px) or relative (em);
  * font-style:         - one of [normal, italic, oblique];
  * font-variant:       - one of [normal, small-caps];
  * font-weight:        - one of [normal, bold];

It may be hard to distinguish oblique text from italic text.

<hr /><!-- Font Family -->

The font family is a comma separated list of font names (from the same font family) terminated by the family name.
The list is a fall-back system:  the first font in the list is preferred but if it is not available,
the next is considered and so on:

```html
    p { font-family: "Times New Roman", Times, serif; }
```

There is a default font for each family but it is system dependent.
There are recommended combinations but they do not look cross-platform.

There are (Google) fonts on-line that are downloaded on the fly.  See Web Fonts below.

<hr /><!-- Font Size -->

The font size is absolute if specified in pixels.
This is viewed as bad for accessibility as the user cannot change the text size.

The font size is relative if specified in ems.
This is relative to surrounding elements.
The user can change the text size should they find it too small to read comfortably.

A text size of 1em is equal to the current font size.
For the sake of some older IE browser, set:

```html
    body { font-size: 100%; }
```

The font size may be doubled up with the line height property as shown below.

<hr /><!-- Shorthand -->

The shorthand `font` property may be used to set several properties in one statement:

```html
    p { font: italic normal bold 12px/30px Georgia, serif; }

```

is equivalent to:

```html
    p {
      font-style:     italic;
      font-variant:   normal;
      font-weight:    bold;
      font-size:      12px/30px;
      font-family:    Georgia, serif;
    }
```

'No change' values may be omitted as along as the values that are given are in the order shown.


## CSS3 Web Fonts

With CSS3, web pages are no longer 'forced' to use only 'web-safe' fonts installed on the client machine.

The `@font-face` rule declares a font that can be downloaded and when to use it.

```css3
@font-face {
    src: url(sansation_light.woff);
    font-family: myFirstFont;
}

@font-face {
    src: url(sansation_bold.woff);
    font-family: myFirstFont;
    font-weight: bold;
}
```

The `src` attributes identify where the font is available for download.
The `font-family` and `font-weight` attributes identify when to use the downloaded font.
In this context, they are referred to as font descriptors.

Note:  yes, the `bold` means render a special version of the font, not render the font in a special way.

The font descriptors that can be used in a `@font-face` rule are:

  * `font-family`       - required - names the font
  * `src`               - required - URL of the font file for download
  * `font-style`        - [normal, italic, oblique]
  * `font-weight`       - [normal, bold, 100, 200, ... 900]
  * `font-stretch`      - [normal, expanded, [, ultra-, extra-, semi-]condensed, [, ultra-, extra-, semi-]expanded]
  * `unicode-range`     - the range of Unicode characters supported, default "U+0-10FFFF"

<hr />

True Type Fonts (TTF) adhere to a standard developed for PCs in the late 1980s by Apple and Microsoft.

OpenType Fonts (OTF) are scalable fonts based on TTF developed by Microsoft.

Web Open Font Format (WOFF) is TTF and OTF with compression for web use from 2009.  A W3C recommendation.
Version 2.0 provides better compression.

SVG fonts allow SVG glyphs to be used when displaying text.
SVG 1.1 allows a font module embedded with an SVG document.
CSS can be applied to SVG documents and `@font-face` to text in SVG documents.

Embedded OpenType Fonts (EOT) compact OTF by Microsoft for use as embedded font on web pages.

Only IE supports EOF.  Mozilla is/was late to support SVG.
</body>
</html>
