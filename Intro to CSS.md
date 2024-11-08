# CSS Introduction

CSS is the language we use to style a Web page.

### What is CSS?

- CSS stands for Cascading Style Sheets
- CSS describes how HTML elements are to be displayed on screen, paper, or in other media
- CSS saves a lot of work. It can control the layout of multiple web pages all at once
- External stylesheets are stored in CSS files.

### Why Use CSS?

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

### CSS Example

``` css
body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

### CSS Solved a Big Problem
HTML was NEVER intended to contain tags for formatting a web page!

HTML was created to describe the content of a web page, like:

`<h1>` This is a heading `</h1>`

`<p>` This is a paragraph. `</p>`

When tags like `<font>`, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process.

To solve this problem, the World Wide Web Consortium (W3C) created CSS.

CSS removed the style formatting from the HTML page!

### CSS Saves a Lot of Work!

The style definitions are normally saved in external .css files.

With an external stylesheet file, you can change the look of an entire website by changing just one file!

# CSS Syntax

### CSS Syntax

A CSS rule consists of a selector and a declaration block.

![css](https://www.w3schools.com/css/img_selector.gif)

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

# HTML Table Borders

### How To Add a Border

To add a border, use the `border` property on `table`, `th`, and `td` elements:

### Example

``` css
table, th, td {
  border: 1px solid black;
}
```

### Collapsed Table Borders

To avoid having double borders like in the example above, set the CSS `border-collapse` property to `collapse`.

This will make the borders collapse into a single border

### Example

``` css
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
```

### Dotted Table Borders

With the `border-style` property, you can set the appearance of the border.

The following values are allowed:

- dotted
- dashed
- solid
- double
- groove
- ridge
- inset
- outset
- none
- hidden

### Example

``` css
 th, td {
  border-style: dotted;
}
```

### Border Color

With the `border-color` property, you can set the color of the border.

### Example

``` css
  th, td {
  border-color: #96D4D4;
}
```

### HTML Table - Cell Padding

Cell padding is the space between the cell edges and the cell content.

By default the padding is set to 0.

To add padding on table cells, use the CSS `padding` property:

### Example

``` css
  th, td {
  padding: 15px;
}
```

To add padding only above the content, use the `padding-top` property.

And the others sides with the `padding-bottom`, `padding-left`, and `padding-right` properties:

### Example

``` css
  th, td {
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 40px;
}
```

### HTML Table - Cell Spacing

Cell spacing is the space between each cell.

By default the space is set to 2 pixels.

To change the space between table cells, use the CSS `border-spacing` property on the table element:

### Example

``` css
  table {
  border-spacing: 30px;
}
```

## HTML Table Styling

### HTML Table - Zebra Stripes

If you add a background color on every other table row, you will get a nice zebra stripes effect.

To style every other table row element, use the `:nth-child(even)` selector like this:

### Example

``` css
tr:nth-child(even) {
  background-color: #D6EEEE;
}
```

**Note:** If you use `(odd)` instead of `(even)`, the styling will occur on row 1,3,5 etc. instead of 2,4,6 etc.

### HTML Table - Vertical Zebra Stripes

To make vertical zebra stripes, style every other column, instead of every other row.

Set the `:nth-child(even)` for table data elements like this:

### Example

``` css
td:nth-child(even), th:nth-child(even) {
  background-color: #D6EEEE;
}
```

**Note:** Put the :nth-child() selector on both th and td elements if you want to have the styling on both headers and regular table cells.


### Combine Vertical and Horizontal Zebra Stripes

You can combine the styling from the two examples above and you will have stripes on every other row and every other column.

If you use a transparent color you will get an overlapping effect.

Use an `rgba()` color to specify the transparency of the color:

### Example

``` css
tr:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}

th:nth-child(even),td:nth-child(even) {
  background-color: rgba(150, 212, 212, 0.4);
}
```

### Horizontal Dividers

If you specify borders only at the bottom of each table row, you will have a table with horizontal dividers.

Add the `border-bottom` property to all `tr` elements to get horizontal dividers:

### Example

``` css
tr {
  border-bottom: 1px solid #ddd;
}
```

### Hoverable Table

Use the :hover selector on tr to highlight table rows on mouse over:

### Example

``` css
tr:hover {background-color: #D6EEEE;}
```

# CSS Selector Reference

A CSS selector selects the HTML element(s) you want to style.

### CSS Selectors

CSS selectors are used to "find" (or select) the HTML elements you want to style.

We can divide CSS selectors into five categories:

- Simple selectors (select elements based on name, id, class)
- Combinator selectors (select elements based on a specific relationship between them)
- Pseudo-class selectors (select elements based on a certain state)
- Pseudo-elements selectors (select and style a part of an element)
- Attribute selectors (select elements based on an attribute or attribute value)

### The CSS element Selector

The element selector selects HTML elements based on the element name.

### Example

Here, all `<p>` elements on the page will be center-aligned, with a red text color: 

``` css
  p {
  text-align: center;
  color: red;
}
```

### The CSS id Selector

The id selector uses the id attribute of an HTML element to select a specific element.

The id of an element is unique within a page, so the id selector is used to select one unique element!

To select an element with a specific id, write a hash (#) character, followed by the id of the element.

### Example

The CSS rule below will be applied to the HTML element with id="para1": 

``` css
  #para1 {
  text-align: center;
  color: red;
}
```

**Note:** An id name cannot start with a number!

### The CSS class Selector

The class selector selects HTML elements with a specific class attribute.

To select elements with a specific class, write a period (.) character, followed by the class name.

### Example

In this example all HTML elements with class="center" will be red and center-aligned: 

``` css
  .center {
  text-align: center;
  color: red;
}
```

**You can also specify that only specific HTML elements should be affected by a class.**

### Example

In this example only `<p>` elements with class="center" will be red and center-aligned: 

``` css
 p.center {
  text-align: center;
  color: red;
}
```

**HTML elements can also refer to more than one class.**

### Example

In this example the <p> element will be styled according to `class="center"` and to `class="large"`:

``` html
<p class="center large">This paragraph refers to two classes.</p>
```

**Note:** A class name cannot start with a number!

### The CSS Universal Selector

The universal selector `(*)` selects all HTML elements on the page.

### Example

The CSS rule below will affect every HTML element on the page: 

``` css
 * {
  text-align: center;
  color: blue;
}
```

### The CSS Grouping Selector

The grouping selector selects all the HTML elements with the same style definitions.

Look at the following CSS code (the h1, h2, and p elements have the same style definitions):

``` css
 h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

It will be better to group the selectors, to minimize the code.

To group selectors, separate each selector with a comma.

### Example

In this example we have grouped the selectors from the code above:

 ``` css
 h1, h2, p {
  text-align: center;
  color: red;
}
```

### All CSS Simple Selectors

| Selector      | Example                                                                                                                                                                   |                   Example description                   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| #id | #firstname |  Selects the element with `id="firstname"` |
| .class | .intro | Selects all elements with `class="intro"` |
| * | * | Selects all elements |
| element | p | Selects all `<p>` elements |
| element,element,.. | div, p | Selects all `<div>` elements and all `<p>` elements |

## What are Pseudo-classes?

A pseudo-class is used to define a special state of an element.

For example, it can be used to:

- Style an element when a user moves the mouse over it
- Style visited and unvisited links differently
- Style an element when it gets focus
- Style valid/invalid/required/optional form elements

### Syntax

The syntax of pseudo-classes:

 ``` css
selector:pseudo-class {
  property: value;
}
```

Few examples of pseudo-classes:

- hover
- active
- first-child

### Hover on `<div>`

An example of using the :hover pseudo-class on a `<div>` element:

 ``` css
div:hover {
  background-color: blue;
}
```

### Active :active pseudo-classes

An example of using the :active pseudo-class on a `<button>` element:

 ``` css
buttton:hover {
  background-color: blue;
}
```

### CSS - The :first-child Pseudo-class

The `:first-child` pseudo-class matches a specified element that is the first child of another element.

### Match the first `<p>` element

In the following example, the selector matches any `<p>` element that is the first child of any element:

 ``` css
p:first-child {
  color: blue;
}
```

## CSS Pseudo-elements

#### What are Pseudo-Elements?

A CSS pseudo-element is used to style specific parts of an element.

For example, it can be used to:

- Style the first letter or line, of an element
- Insert content before or after an element
- Style the markers of list items
- Style the viewbox behind a dialog box

### Syntax

The syntax of pseudo-elements:

 ``` css
selector::pseudo-element {
  property: value;
}
```

### The ::first-line Pseudo-element

The `::first-line` pseudo-element is used to add a special style to the first line of a text.

The following example formats the first line of the text in all `<p>` elements:

 ``` css
p::first-line {
  color: #ff0000;
  font-variant: small-caps;
}
```

**Note:** The `::first-line` pseudo-element can only be applied to block-level elements.

The following properties apply to the ::first-line pseudo-element:

- font properties
- color properties
- background properties
- word-spacing
- letter-spacing
- text-decoration
- vertical-align
- text-transform
- line-height
- clear

**Notice the double colon notation** - `::first-line` versus `:first-line`

The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between **pseudo-classes** and **pseudo-elements**.

The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1.

For backward compatibility, the single-colon syntax is acceptable for CSS2 and CSS1 pseudo-elements.

### The ::first-letter Pseudo-element

The `::first-letter` pseudo-element is used to add a special style to the first letter of a text.

The following example formats the first letter of the text in all `<p>` elements: 

### Example

 ``` css
p::first-letter {
  color: #ff0000;
  font-size: xx-large;
}
```

**Note:** The `::first-letter` pseudo-element can only be applied to block-level elements.

The following properties apply to the `::first-letter` pseudo- element: 

- font properties
- color properties 
- background properties
- margin properties
- padding properties
- border properties
- text-decoration
- vertical-align (only if "float" is "none")
- text-transform
- line-height
- float
- clear

### CSS - The ::before Pseudo-element

The `::before` pseudo-element can be used to insert some content before the content of an element.

The following example inserts an image before the content of each `<h1>` element:

### Example

 ``` css
h1::before {
  content: "1";
}
```

### CSS - The ::after Pseudo-element

The `::after` pseudo-element can be used to insert some content after the content of an element.

The following example inserts an image after the content of each `<h1>` element:

### Example

 ``` css
h1::before {
  content: "1";
}
```

### CSS - The ::marker Pseudo-element

The `::marker` pseudo-element selects the markers of list items.

The following example styles the markers of list items:

### Example

 ``` css
::marker {
  color: red;
  font-size: 23px;
}
```

### CSS - The ::selection Pseudo-element

The `::selection` pseudo-element matches the portion of an element that is selected by a user.

The following CSS properties can be applied to `::selection: color, background, cursor, and outline`.

The following example makes the selected text red on a yellow background:

### Example

 ``` css
::selection {
  color: red;
  background: yellow;
}
```