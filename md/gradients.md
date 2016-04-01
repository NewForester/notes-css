<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Gradients

CSS3 gradient allow a background to transition smoothly between two or more colours.
Before these, background image were used but these required significant bandwidth and did not always zoom well.

There are four gradient properties:

  * linear-gradient             - the transition is across and/or down the element box
  * radial-gradient             - the transition is outwards from the centre
  * repeating-linear-gradient   - the transition reverses and repeats itself
  * repeating-radial-gradient   - the transition reverses and repeats itself

Their syntax is rather like a function call (in most programming languages):

```css3
     background: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);
```

A gradient requires at least two colour stops:  the transition being from the first to the second.
There may be more just as a journey may have stopping points as well as a start and a final destination.

There is also the direction of the transition.
By default, the transition is `top`, which means top to bottom.
You can also use `to top`, `to right`, `to left` and `to bottom`.

It is also possible to have a diagonal gradient.
Specify the corner to which the gradient is to transition.
Try `to bottom right` etc.

For finer control, you can give the gradient in degrees.
`0deg`, `90deg`, `180deg` and `-90deg` are the same as `to top` etc.

By using RGBA or HSLA colours you can transition from transparent to opaque without changing colour.

By using several colour stops you can achieve a rainbow effect.

<style>
#grad1 {
    height: 55px;
    background: linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet);
}
</style>
</head>
<body>

<div id="grad1" style="text-align:center;margin:auto;color:#888888;font-size:40px;font-weight:bold">
</div>

By default, the colour stops are equally spaced but the use of percentages can alter this.
How to choose the values other than by trial and error is not known at this time.

How the `repeating-linear-gradient` works is not clear.
Certainly it seems the first colour must not have a percentage.

The syntax for the radial gradients is:

```css
    background: radial-gradient(shape size at position, start-colour, ..., last-colour);
```

The default shape is `ellipse`, the alternative is `circle`.

The size is one of:

  * closest-side
  * farthest-side
  * closet-corner
  * farthest-corner

with, it seems the interpretation, the 'transition ends here'.

The position is the centre from which the gradient radiates.
Two percentages give the centre with respect to the element's box.

</body>
</html>
