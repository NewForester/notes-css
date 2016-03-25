<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS and Forms

The appearance of HTML forms can be greatly improved through judicious use of CSS.

Often attribute selectors are used:

  * `input[type=text]           - styling for text fields
  * `input[type=password]       - styling for password fields
  * `input[type=number]         - styling for number fields
  * etc.

Style properties often set for form fields include:

  * width;
  * padding and margin;
  * border and border-radius;
  * background-color and (text) color;

Note:  with CSS3 is it common to include the padding and borders in the total width and height of input fields
using `box-sizing: border-box;`.

Menus created using the `<select>` element can be styled directly.

By default, a text area has a 'grabber' in the bottom right hand corner that allows the field to be resized.
Use `resize: none;` to disallow this.  The text area will still sprout a vertical scroll bar as necessary.

Input buttons might well be styled as a group:

```css
    input[type=button], input[type=submit], input[type=reset] { ... }
```

<hr />

Highlighting the field with 'focus' is common.

By default, some browsers add a blue line around the field focus.
You may remove this with `outline: none;`.

You may add you own highlighting by changing the field's border or background colour as in:

```css
    input[type=text]:focus {
        background-color: lightblue;
    }
```

An icon (such as a search icon) can be placed inside an input field using the background property.
Use the `padding` attribute to make way for the icon.

Using features new with CSS3, a transition effect can be made to occur when an input field gains focus.

Here is example CSS3:

```css
    input[type=text] {
        box-sizing: border-box;
        border: 2px solid #ccc;
        border-radius: 4px;
        font-size: 16px;

        background-color: white;
        background-image: url('../images/searchicon.png');
        background-position: 10px 10px;
        background-repeat: no-repeat;
        padding: 12px 20px 12px 40px;

        width: 130px;
        transition: width 0.4s ease-in-out;
    }

    input[type=text]:focus {
        width: 100%;
    }
```

The example HTML is simple:

```html
    <form>
        <input type="text" name="search" placeholder="Search...">
    </form>
```

will appear as:

<style>
    input[type=text] {
        width: 130px;
        box-sizing: border-box;
        border: 2px solid #ccc;
        border-radius: 4px;
        font-size: 16px;
        background-color: white;
        background-image: url('../images/searchicon.png');
        background-position: 10px 10px;
        background-repeat: no-repeat;
        padding: 12px 20px 12px 40px;
        -webkit-transition: width 0.4s ease-in-out;
        transition: width 0.4s ease-in-out;
    }

    input[type=text]:focus {
        width: 100%;
    }
</style>

<div class=indent>
    <form>
        <input type="text" name="search" placeholder="Search...">
    </form>
</div>

</body>
</html>
