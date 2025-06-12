# Background

```css
div {
  background-color: #f0f8ff;
  background-image: url('background.jpg');
  background-repeat: no-repeat;
  background-position: center top;
  background-size: cover;
  background-attachment: fixed;
  background-origin: padding-box;
  background-clip: border-box;
}
```

# Border & Outline

```css
div {

  /* BORDER */
  border-width: 2px;
  border-style: solid;
  border-color: #007bff;
  border-radius: 8px;

  /* OUTLINE */
  outline-width: 3px;
  outline-style: dashed;
  outline-color: red;
  outline-offset: 4px;
  
  /* SHORTCUT */
  border: 2px solid #007bff;
  outline: 3px dashed red;
}
```

# Font & Text

```css
div {
  /* FONT */
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px;
  font-style: italic;
  font-weight: 600;
  font-variant: small-caps;
  font-stretch: expanded;

  /* TEXT */
  color: #333;
  text-align: justify;
  text-decoration: underline dotted red;
  text-transform: capitalize;
  text-indent: 2em;
  letter-spacing: 1px;
  word-spacing: 5px;
  line-height: 1.6;
  white-space: nowrap;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
  direction: ltr;
  writing-mode: horizontal-tb;
}
```

# Padding & Margin

```css
div {
  /* MARGIN */
  margin: 20px;
  margin-top: 10px;
  margin-right: 15px;
  margin-bottom: 20px;
  margin-left: 25px;

  /* PADDING */
  padding: 30px;
  padding-top: 10px;
  padding-right: 20px;
  padding-bottom: 15px;
  padding-left: 25px;
}
```

# Flex

### Parent

```css
.parent-container {
  display: flex;
  flex-direction: row;
  /* Main axis direction 
        - row
        - row-reverse
        - column
        - column-reverse)
    */
  flex-wrap: wrap;
  /* Allows wrapping 
        - nowrap
        - wrap
        - wrap-reverse
    */
  justify-content: space-between; 
  /* Horizontal alignment 
        - start
        - center
        - end
        - space-between
        - space-around
        - space-evenly
    */
  align-items: center;
  /* Vertical alignment of items 
        - start
        - center
        - end
        - stretch
        - ...
    */
  align-content: stretch; 
  /* Alignment of lines when wrapping (works like align-items, but for lines) */
  gap: 10px;
  row-gap: 15px;
  column-gap: 20px;
}
```
### Child

```css
.child-item {
  flex: 1 1 auto;      /* flex-grow, flex-shrink, flex-basis shorthand */
  order: 0;            /* Defines the order of the item */
  align-self: auto;    /* Overrides align-items for individual item */
}

```

# Grid

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 100px auto;
  grid-template-areas:
    "header header header"
    "sidebar content content";
  grid-column-gap: 20px;
  grid-row-gap: 10px;
  gap: 10px 20px;
  justify-items: center;
  align-items: stretch;
  justify-content: space-between;
  align-content: start;
  grid-auto-flow: row dense;
  grid-auto-rows: minmax(100px, auto);
  grid-auto-columns: 200px;
}
```