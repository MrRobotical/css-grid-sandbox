This repo cointains 4 projects built from the NetNija Tutorials to learn and practice CSS Grid Concepts.

CSS Grid Cheat Sheet
1. Define a Grid Container
Use display: grid to make an element a grid container.

.container {
  display: grid;
}
2. Define Columns and Rows
Use grid-template-columns and grid-template-rows to set the number and size of columns and rows.

.container {
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto 100px;
}
3. Grid Item Placement
Use grid-column and grid-row to place grid items within the grid.

.item {
  grid-column: 1 / 3;  /* Start at column 1, end at column 3 */
  grid-row: 2 / 4;     /* Start at row 2, end at row 4 */
}
4. Gap Between Items
Use gap, column-gap, and row-gap to set the spacing between grid items.

.container {
  gap: 10px;  /* Sets both row and column gaps */
}
5. Repeat Function
Use repeat() to avoid redundancy in defining rows or columns.

.container {
  grid-template-columns: repeat(3, 1fr);
}
6. Auto-fill and Auto-fit
Use auto-fill and auto-fit with repeat() for responsive grids.

.container {
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}
7. Minmax Function
Use minmax(min, max) to set a size range for grid tracks.

.container {
  grid-template-columns: repeat(3, minmax(100px, 1fr));
}
8. Grid Template Areas
Define named grid areas for easier item placement.

.container {
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}
.header {
  grid-area: header;
}
9. Implicit Grid
Items placed outside the explicit grid create implicit tracks.

.item {
  grid-column: 5;  /* Implicitly creates columns 3 and 4 */
}
10. Align and Justify Items
Use align-items, justify-items, align-content, and justify-content to control alignment.

.container {
  align-items: center;
  justify-content: center;
}
Bonus: Fractional Units (fr)
Use fr to define flexible grid tracks that distribute available space.

.container {
  grid-template-columns: 1fr 2fr;
}
Bonus: Media Queries
Combine grid with media queries for responsive design.

@media (max-width: 600px) {
  .container {
    grid-template-columns: 1fr;
  }
}
Practical Example
Here’s a simple example demonstrating these key concepts:

html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    gap: 10px;
  }
  .item {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
  }
</style>
</head>
<body>
  <div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
  </div>
</body>
</html>
