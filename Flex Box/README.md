# CSS Flexbox

### CSS Flexbox Layout Module

Before the Flexbox Layout module, there were four layout modes:

- Block, for sections in a webpage
- Inline, for text
- Table, for two-dimensional table data
- Positioned, for explicit position of an element
The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.

### Flexbox Elements

To start using the Flexbox model, you need to first define a flex container.

### Example 

A flex container with three flex items:

```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

## CSS Flex Container

### Parent Element (Container)

Like we specified in the previous chapter, this is a flex container (the blue area) with three flex `items`:

The flex container becomes flexible by setting the display property to `flex`:

### Example 

```css
.flex-container {
  display: flex;
}
```

The flex container properties are:

- `flex-direction`
- `flex-wrap`
- `flex-flow`
- `justify-content`
- `align-items`
- `align-content`

### The flex-direction Property

The `flex-direction` property defines in which direction the container wants to stack the flex items.

### Example 

The `column` value stacks the flex items vertically (from top to bottom):

```css
.flex-container {
  display: flex;
  flex-direction: column;
}
```

### Example 

The `column-reverse` value stacks the flex items vertically (but from bottom to top):

```css
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```

### Example 

The `row` value stacks the flex items horizontally (from left to right):

```css
.flex-container {
  display: flex;
  flex-direction: row;
}
```

### Example 

The `row-reverse` value stacks the flex items horizontally (but from right to left):

```css
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
```

### The flex-wrap Property

The `flex-wrap` property specifies whether the flex items should wrap or not.

The examples below have 12 flex items, to better demonstrate the `flex-wrap` property.

### Example 

The `wrap` value specifies that the flex items will wrap if necessary:

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```

### Example 

The `nowrap` value specifies that the flex items will not wrap (this is default):

```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
```

### Example 

The `wrap-reverse` value specifies that the flexible items will wrap if necessary, in reverse order:

```css
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```

### The flex-flow Property

The `flex-flow` property is a shorthand property for setting both the `flex-direction` and `flex-wrap` properties.

### Example 

```css
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
```

### The justify-content Property

The `justify-content` property is used to align the flex items:

### Example 

```css
.flex-container {
  display: flex;
  justify-content: center;
}
```

### Example 

The `flex-start` value aligns the flex items at the beginning of the container (this is default):

```css
.flex-container {
  display: flex;
  justify-content: flex-start;
}
```

### Example 

The `flex-end` value aligns the flex items at the end of the container:

```css
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```

### Example 

The `space-around` value displays the flex items with space before, between, and after the lines:

```css
.flex-container {
  display: flex;
  justify-content: space-around;
}
```

### Example 

The `space-between` value displays the flex items with space between the lines:

```css
.flex-container {
  display: flex;
  justify-content: space-between;
}
```

### The align-items Property

The align-items property is used to align the flex items.

In these examples we use a 200 pixels high container, to better demonstrate the align-items property.

### Example 

The `center` value aligns the flex items in the middle of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: center;
}
```

### Example 

The `flex-start` value aligns the flex items at the top of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-start;
}
```

### Example 

The `flex-end` value aligns the flex items at the bottom of the container:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: flex-end;
}
```

### Example 

The `stretch` value stretches the flex items to fill the container (this is default):

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: stretch;
}
```

### Example 

The `baseline` value aligns the flex items such as their baselines aligns:

```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: baseline;
}
```

**Note:** the example uses different font-size to demonstrate that the items gets aligned by the text baseline
