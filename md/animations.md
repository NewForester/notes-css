<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Animations

CSS3 animations allow the animation of many elements without using scripts.
They resemble CSS transitions but allow more sophisticated effects.

The examples in the tutorial involve changing the background colour of a box while moving it around the page.

There is no trigger:  the animation occurs on page load.
However, I guess they could be triggered by events or scripts.

There are six properties with one summary property:

  * `animation-name`                    - the name a of @keyframes code animation block
  * `animation-duration`                - how long the effect lasts (seconds)
  * `animation-timing-function`         - the speed curve of the animation effect
  * `animation-delay`                   - how long before the animation starts (seconds)
  * `animation-iteration-count`         - how may times to repeat the animation
  * `animation-direction`               - play in reverse or alternate through repetitions

The summary property has the form:

```css3
    animation: name duration timing-function delay iteration-count direction
```

There are two further properties not covered by the tutorial.

  * `animation-fill-mode`               - the element style when the animation is not running
  * `animation-play-state`              - whether the animation if running or not

A value must be given for the duration.  Nothing will happen otherwise as the duration defaults to 0.


The `animation-timing-function` is one of:

  * ease                        - default - as `ease-in-out` but with more aggressive acceleration;
  * linear                      - the animation proceeds with a constant speed;
  * ease-in                     - the animation starts slowly and speeds up;
  * ease-out                    - the animation starts fast and slows down towards the end;
  * ease-in-out                 - the animation is slower at the start and end than in between;
  * cubic-bezier(n,n,n,n)       - define your own values for a cubic Bezier function;

I guess the `cubic-bezier()` is for experts.

The iteration determines how many times the animation should be run.
The examples use integers or the value `infinite`.

The direction may take the value `normal`, `reverse`, `alternate` and `alternate-reverse` as well as `initial` and `inherit`.

<hr />

An important difference between transitions and animations is that a transition refer to one or more properties while
an animation refers to a bit of code called a keyframe that may refer to several properties.

A simple example that specifies just initial and final states is:

```css
    @keyframes name {
        from {background-color; red; }
        to   {background-color; yellow; }
    }
```

A more complex example specifies a series of states using percentages of the animation's duration:

```css
    @keyframe name {
          0%    { background-color: red;    left:  0px; top:  0px; }
         25%    { background-color: yellow; left: 50px; top:  0px; }
         50%    { background-color: blue;   left: 50px; top: 50px; }
         75%    { background-color: green;  left:  0px; top: 50px; }
        100%    { background-color: red;    left:  0px; top:  0px; }
    }
```

</body>
</html>
