## Notes from WDF's Emmet vid
>Emmet can help save me a ton of time writing repeatitive HTML code

- Emmet is built-in in VScode.
- Much of the shortcuts I already know.

>Generate HTML boilerplate
```
! + `Enter`
```
 
 >We can create child elements as well:
 ```html
 div.purple>span.cyan

 <!-- will generate -->
 class `purple` div wih `cyan` as a span child

 <!-- can continue on -->
 header>nav>ul>li*4
 header>nav>ul>4 li
```
>Adding placeholder texts inside the elements
```html
li*3{list item}

<!-- all 3 lis will have the same text -->
```
>Showing up numbers in the element(incrementation) using `$`:
```html
nav>ul>li{list item $}

will go like list item1,list item2, list item3($ will get incremented)
```
We can also use `$` for classes as well:
```html
nav>ul>li>.div-$
<!-- will generate -->
div1 div2 div3 classes
```
If we add more `$`, more and more `0`s will be added at the start like 01,001,0001.

### Creating Siblings
>Use `+` for creating siblings
```html
header+main+footer
<!-- will generate -->
<header></header>
<main></main>
<footer></footer>
```
Adding children to sibling(s).
header>nav^main>div.div1^footer

header > nav
main > div1
footer
```
Or to be simpler, we can use group operators, parenthesises as well.
```html
(header>nav)+(main>div1)+footer
```
<!-- The sample -->
<!-- (header>h2(heading)+nav>ol>li*5>a{link $}) -->
