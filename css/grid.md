## Traversy's Grid Crash Course Here we go

> ### Difference between Flexbox and Grid
- Flexbox is one dimensional.
- Grid is two dimensional.

__*Notes and Code in "**cssgrid.html, cssgrid1.html**", "**grid.css**".*__

- We can add *'gaps'* inside the divs by using: 
```css
grid-column-gap: 10px;

grid-row-gap: 30px;

/* or */

grid-gap: 1em; /*for both*/
```
---
- Adding grid widths or grid-template....:
```css
grid-template-columns: 1fr 1fr 2fr;

grid-template-rows: 2fr 3fr;

/* or */
grid-template-columns:repeat(3, 1fr);

grid-template-rows:repeat(4, 2fr);

/* or */
grid-template-columns:repeat(3, 1fr 2fr); /*1fr 2fr 1fr 2fr .... */

grid-template-rows:repeat(4, 2fr 3fr);
```
---
- Height of each grid box:
```css
grid-auto-rows: 100px;

grid-auto-columns: 100px; 
```
*They are fixed tho so the content will overflow if not fit.*
*To prevent that, we can use **minmax()***:
```css
grid-auto-rows: minmax(100px, auto);

grid-auto-columns: minmax(100px, auto);
```
*basically adding min and max heights.*

*When added minmax(), the entire row/column will stretch out if the content max out.*

---

I will continue later on about 4mins left
ONto the project