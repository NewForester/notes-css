<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS3 Transitions

CSS3 transitions allow the rendering of property values to change smoothly.

The examples in the tutorial are all change the width of an element or apply a transform.
I do not know if the property apply to all attributes or just those that can be animated.
I am not sure what I would be looking for if I set a transition time on changing text style from
normal to italic.

The example all use mouse hover to trigger the transition (and back again).
I guess you can use scripts too.

There are four properties and one summary property:

  * `transition-property`               - the name the CSS property whose value is to be transitioned
  * `transition-duration`               - how long the effect lasts (seconds)
  * `transition-timing-function`        - the speed curve of the transition effect
  * `transition-delay`                  - how long before the transition starts (seconds)

The summary property has the form:

```css3
    transition: property duration timing-function delay
```

for a single property and

```css3
    transition: property duration timing-function delay, property2 duration2 timing-function2 delay2, ...
```

for more than one.

A value must be given for the duration.  Nothing will happen otherwise as the duration defaults to 0.

The `transition-timing-function` is one of:

  * ease                        - default - as `ease-in-out` but with more aggressive acceleration;
  * linear                      - the transition proceeds with a constant speed;
  * ease-in                     - the transition starts slowly and speeds up;
  * ease-out                    - the transition starts fast and slows down towards the end;
  * ease-in-out                 - the transition is slower at the start and end than in between;
  * cubic-bezier(n,n,n,n)       - define your own values for a cubic Bezier function;

I guess the `cubic-bezier()` is for experts.

</body>
</html>
