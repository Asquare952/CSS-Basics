# CSS Specificity

### What is Specificity?

If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element.

Think of specificity as a score/rank that determines which style declaration is ultimately applied to an element.

Look at the following examples:

### Example 1

In this example, we have used the "p" element as selector, and specified a red color for this element. The text will be red:

```html
<html>
<head>
  <style>
    p {color: red;}
  </style>
</head>
<body>

<p>Hello World!</p>

</body>
</html>
```

Now, look at example 2:

### Example 2

In this example, we have added a class selector (named "test"), and specified a green color for this class. The text will now be green (even though we have specified a red color for the element selector "p"). This is because the class selector is given higher priority:

```html
<html>
<head>
  <style>
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p class="test">Hello World!</p>

</body>
</html>
```

Now, look at example 3:

### Example 3

In this example, we have added the id selector (named "demo"). The text will now be blue, because the id selector is given higher priority:

```html
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test">Hello World!</p>

</body>
</html>
```

Now, look at example 3:

### Example 4

In this example, we have added an inline style for the "p" element. The text will now be pink, because the inline style is given the highest priority:

```html
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test" style="color: pink;">Hello World!</p>

</body>
</html>
```

### Specificity Hierarchy

Every CSS selector has its place in the specificity hierarchy.

There are four categories which define the specificity level of a selector:

1. **Inline styles** - Example: `<h1 style="color: pink;">`
2. **IDs** - Example: `#navbar`
3. **Classes, pseudo-classes, attribute selectors** - Example: `.test`, `:hover`, `[href]`
4. **Elements and pseudo-elements** - Example: `h1`, `::before`