<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Pseudo Classes

Pseudo classes are defined in term of elements and their state.

The syntax for pseudo classes is:

```css
    selector:pseudo-class { property:value; ... }
```

Note that any selector can be combined with a pseudo class:

```css
    a.highlight:hover { color: #ff0000; }
```

A good many pseudo classes are specific to a particular element.
Many are specific to input elements.

One pseudo-class that may be combined with any element is `:hover`,
which is active which the mouse hovers over the element.

<hr /><!-- Anchor pseudo classes -->

There are four pseudo classes for hyper-link `<a>` element:

  *  a:link     - a normal, unvisited link
  *  a:visited  - a link the user has visited
  *  a:hover    - a link when the user mouses over it
  *  a:active   - a link the moment it is clicked

The properties for the individual states must declared in the order above.
These may be discussed in more details on the [CSS Links](links.html) page.

<hr /><!-- First Child pseudo class -->

The `:first-child` pseudo-class matches the first child of the containing element:

```css
    p:first-child       { ... }         /* any <p> that is the first child of any other element */
    p i:first-child     { ... }         /* first <i> element of all <p> elements */
    p:first-child i     { ... }         /* all <i> elements of any <p> element that is a first child */
```

<hr /><!-- Lang pseudo class -->

The `:lang` pseudo classes allow different rules for different languages.
An example is changing the quotation marks for `<q>` elements.

```html
    <style>
      q:lang(fr) {
        quotes: "«" "»";
      }
    </style>

    <body>
      <p>Some text <q lang="fr">Salut!</q> Some text.</p>
    </body>
```

</body>
</html>
