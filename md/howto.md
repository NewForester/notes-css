<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS How To

There are three ways style information can be added to HTML:

  * external style sheet
  * internal style sheet
  * in-line styles

An external style sheet is the most common as it allows all pages of the same web site to have the same styles.
They are included using a `<link>` element within the `<head>` element.
They must be files with the extension '.css'.

```html
    <head>
      <link rel="stylesheet" type="text/css" href="styles.css" />
    </head>
```

The internal style sheet is the `<style>` element within the `<head>` element.
Such style definitions are local to the one HTML document.

```html
    <head>
      <style>
        <!-- whatever might go in an external style sheet -->
      </style>
    </head>
```

In-line styles are added to individual HTML elements using the `style=` attribute.
Such style definitions apply the element and its nested elements.

```html
    <p style="a list of property:value; pairs">A paragraph with in-line style</p>
```

The term cascading refers to rules that:

  * in-line styles take precedence of style sheets and
  * style sheets take precedence over the browser's default styles.

It is normal to want an internal style sheet to take precedence over an external style sheet:
in the `<head>` element, place the internal style sheet definition after the link to the external style sheet.

When more than one external style sheet is included in a document, each takes precedence over those already read.
So the first and last in the `<head>` element have lowest and highest precedence, respectively.

</body>
</html>
