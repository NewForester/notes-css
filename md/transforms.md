<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

The tutorial does not cover 2D and 3D transitions well.
I will have to rewrite this page from scratch someday.

## CSS3 2D Transforms

Elements may be translated (moved), rotated, scaled and skewed using CSS transforms.

Transforms in two dimensions are within the X-Y axis of the web-page.

The syntax is that of a function:

```css
    transform: rotate(20deg);
```

This will rotate the element 20&deg; clockwise.
A negative value will rotate anti-clockwise.

The rotation is done within the X-Y plane of the page and so is the same as the 3D rotation about the Z-axis.

While you might expect the rotation to be about the 'centre' of the element this may not be what happens in practice.
I suspect that the rotation is followed by an implicit translation is done to keep the rotated element within its containing object.

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


## CSS3 3D Transforms

Only the 3D rotations are described and then only briefly.

While the 2D transforms all operate in the X-Y plane that is the web page, the 3D transforms operate in X-Y-Z space.
This is perhaps easiest to visualise with rotation.

The 3D `rotateZ()` is the same as the 2D `rotate()`.
The image stays flat on the web-page.
Rotation by 180&deg; leaves text upside down and back-to-front.

In contrast, think of `rotateY()` as swivelling the monitor around on its base only
it is the element contents, not the entire web page, that rotates.
A rotation of 90&deg; makes the element disappear as you are looking at it end on.
A rotation of 180&deg; leaves text back-to-front.

Think of `rotateX()` as turning the monitor upside down.
A rotation of 90&deg; makes the element disappear as you are looking at it end on.
A rotation of 180&deg; leaves text upside down.

To the list of simple 2D transforms are added `translateZ()` and `scaleZ()` (but not skewZ()) and
to the list of summary transforms is added `translate3d()`, `scale3d()`, `rotate3d()` and `matrix3d()`.

It must be remarked that `rotate3d()` appears to have four parameters of which only one is an angle and
that `matrix3d` takes 16 parameters representing not a 3x3 transform but a 4x4 transform.

One more method is listed: `perspective()` and three more new properties:
`transform-style`, `perspective`, `perspective-origin` and `backface-visibility`.

Clearly there is much experimentation to be done.

</body>
</html>
