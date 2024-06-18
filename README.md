# PROJECT DOCUMENTATION

## CSS

### 1. `.even-columns` class

The `.even-columns` class is designed to create a responsive grid layout. Here's a breakdown of its functionality:

1. **Outside the media query:**

```css
.even-columns {
  display: grid;
  gap: 1rem;
}
```

This sets up a grid layout for any element with the `.even-columns` class. The `gap` property sets a 1rem gap between grid items.

2. **Inside the media query:**

```css
@media (width >= 80em) {
  .even-columns {
    grid-auto-flow: column;
    grid-auto-columns: 1fr;
  }
}
```

This media query applies when the viewport width is 80em or wider. For elements with the `.even-columns` class, it changes the grid layout in two ways:

- `grid-auto-flow: column;` changes the direction in which new grid items are added. Outside the media query, the default value is `row`, so new items are added in new rows. Inside the media query, new items are added in new columns. This is useful for wide screens, where horizontal space is plentiful.

- `grid-auto-columns: 1fr;` sets the size of implicitly created columns. If there are more grid items than cells defined in your grid template, this property controls the size of the columns that are automatically created to accommodate those extra items. By setting it to `1fr`, you're telling the browser to make these implicitly created columns take up an equal share of the available space. This ensures that all columns have equal width, regardless of the number of items.

In summary, the `.even-columns` class creates a responsive grid layout that adjusts based on the viewport width. On narrow screens, grid items are stacked in rows. On wide screens, grid items are placed in columns of equal width.