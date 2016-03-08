<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Syntax

The syntax for a CSS rule set consists of a selector and a declaration block.

```css
    selector {property:value; ...}
```

Lower case is preferred.

The declaration block is a non-empty list of property-value pairs each terminated with a semi-colon.
Often there is a space between the colon and the value but this is optional.

Quote values only when they contain spaces.
There is no space between a value and its units:  `20px` not `20 px`.

The selectors take several forms:

  * an HTML element - is the element name
  * an id - has the form `#xyz` where some (one) element has the attribute `id=xyz`
  * a class selector - has the form `.class`
  * a class and element selector - has the form `element.class`
  * a sub element selector - has the form `element sub-element ...`
  * a grouping selector - has the form `selector1, selector2, ...`

Examples:

```css
    p           { ... }
    #p1         { ... }
    .center     { ... }
    p.center    { ... }
    h1, h2, p   { ... }
```

An element may have more than one class, in which case, both apply.

Styling rules are applied in the order in which they are encountered reading the page and any included style sheets
from top to bottom.

Later rules override earlier rules and rules that do not conflict accumulate.

CSS accepts C-style comments (`/* ... */`), which may spread over several lines but do not nest.

</body>
</html>
