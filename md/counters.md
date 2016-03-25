<!DOCTYPE html>
<html>

<link rel="stylesheet" href="../styles/style-sheet.css" />

<body>

# CSS3

## CSS Counters

CSS counters are simple accumulators for simple tasks like generating section numbers.
They are not general purpose 'variables'.

They can be reset and incremented but they cannot even be assigned an initial value.
Beyond numbering sequences such as header and perhaps lists,
they look like a solution in search of a problem.

Here is an example that increments section and subsection numbers and automatically inserts
them into headers:

```css
    body {
        counter-reset: section;
    }

    h1 {
        counter-reset: subsection;
    }

    h1::before {
        counter-increment: section;
        content: "Section " counter(section) ". ";
    }

    h2::before {
        counter-increment: subsection;
        content: counter(section) "." counter(subsection) " ";
    }
```

Here is an unrealistic example of numbering (nested) list items:

```css
    ol {
        counter-reset: section;
        list-style-type: none;
    }

    li::before {
        counter-increment: section;
        content: counters(section,".") " ";
    }
```

Note the use of `counters(name,separator)` instead of `counter(name)`.

</body>
</html>
