# Grid


### Example :

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