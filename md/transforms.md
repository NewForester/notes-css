<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Transforms

Elements may be translated (moved), rotated, scaled and skewed using CSS transforms.

Transforms in two dimensions are within the x-y axis of the web-page.

The syntax is again that of a function:

```css
    transform: rotate(20deg);
```

This will rotate the element 20° clockwise.
A negative value will rotate anti-clockwise.

While you might expect the rotation to be about the 'centre' of the element this may not be what happens in practice.
I suspect this is done and then an implicit translation is done to keep the rotated element within its containing object.

All the 2D transform methods can be combined into one `matrix` transform
(according to the tutorial - it is not self-evident that rotation is included):

```css
    transform:  matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY()):
```

Yes, the order is correct.

The `matrix` transform may be thought of as a summary transform for:

```ccs
    transform:  scale(X,Y)      # factor to scale by
    transform:  skew(X,Y)       # degrees to skew by
    transform:  translate(X,Y)  # pixels to move the element by
```

These are themselves summary transforms for `scaleX()` ... `translateY()`.

I'm not entirely clear about the units and the effect may not always be what you expect.

There is a second property `transform-origin` which requires the first.
It is not covered by the tutorial at all.

</body>
</html>
