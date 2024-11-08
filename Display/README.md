# CSS Layout - The display Property

The `display` property is the most important CSS property for controlling layout.

### The display Property

The `display` property is used to specify how an element is shown on a web page.

Every HTML element has a default display value, depending on what type of element it is. The default display value for most elements is `block` or `inline`.

The display property is used to change the default display behavior of HTML elements.

### Block-level Elements

A block-level element ALWAYS starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

The `<div>` element is a block-level element.
Examples of block-level elements:

- `<div>`
- `<h1> - <h6>`
- `<p>`
- `<form>`
- `<header>`
- `<footer>`
- `<section>`

### Inline Elements

An inline element DOES NOT start on a new line and only takes up as much width as necessary.

This is an inline `<span>` element inside a paragraph.

Examples of inline elements:

- `<span>`
- `<a>`
- `<img>`

### The display Property Values

The display property has many values:

| Values      |       Description                                                                                                                                                             |                                      |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| inline | Displays an element as an inline element |  
| block | Displays an element as a block element |
| contents | Makes the container disappear, making the child elements children of the element the next level up in the DOM |
| flex | Displays an element as a block-level flex container |
| grid | Displays an element as a block-level grid container |
| inline-block | Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values |
| inline-flex | Displays an element as an inline-level flex container |
| inline-grid | Displays an element as an inline-level grid container |

