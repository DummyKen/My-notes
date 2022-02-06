### Notes from Brad's CSS flexbox crash course
---Here we gooooo---

Flexbox - a css layout providing an easy and clean way to arrange items within a container.

Advantages:
- No Floats
- responsive and mobile friendly
- much easier positioning of child elements
- flex container's margins do not collapse the contents' margins
- order of elements can easily be changed without editing the source HTML

---
- Built for small-scale layouts with 'Grid' for large scale layouts
 
- 'display:flex' and the elements are now flex-items. 
- x and y axis(also as main and cross axis)

__**Syntax:**__
```CSS
display: flex | inline-flex

flex-direction: row | column

flex-wrap: wrap | nowrap | wrapreverse

flex-basis(width): <length>

justify-content: flex-start(left) | flex-end(right) | center

align-self: flex-start | flex-end | center

align-content: flex-start | flex-end | center

flex-grow: <number>;

flex-shrink: <number>;

flex: <integer>;

order: <integer>;
```

*__Coding time__* 

    - cssflex.html
    - cssflex.css
---
- We can add flexbox width for each flex items with:
```css
.box1{
    flex: 3;
}
.box2{
    flex: 2;
}
```
*__box1__* will take 3/5 of the page and the rest will be *__box2__*

- We can also change the order of the flex items:
```css
.box3{
    order: 1;
}
```
*__box3__* will now at the top of the page(flexbox)

**__We need to add order to every item tho__**

- We can align the flex-items to __flex-start/end__.
```css
align-items: flex-start | flex-end;
```
- The (border)box will move along as well.
---
- We can change the flex direction as well:
    - Horizontal --> Row
    - Vertical --> Column
    - Others(rowreverse,columnreverse,inherit,initial,...)
```css
flex-direction: row | column;
```
*Might be really useful in making it responsive on mobile*

- We can justify contents even tho we also gave them widths to each.(*just like text-align but we're aligning divs*)  
    - *flex-start*/*flex-end*/*center*
    - *space-between* if we want to separate each of the items with margins inbetween(~~will fill up the page~~)
    - *space-around* for putting margins on the sides

---
**__And Doneee__**
---

