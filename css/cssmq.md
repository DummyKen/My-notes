# Notes from [WDS](https://youtu.be/yU7jJ3NbPdA?list=TLPQMTIxMjIwMjEdglL3IyoAHg)'s CSS media queries vid

### Here we go

I have been doing projects using this for so long but never got a chance to dive in so here I go.

## Steps in making a site mobile responsive

- add a media query
```css
@media
```
- add a purpose
  - print
  - screen
- normally all purposes.
```css
@media all 
```
- add a max-width as usual

```css
@media all and (max-width: 500px){
    color: blue;
    background-color: black;
}
```
*what it does is that when all these values(*all and the width*) are true then they do these changes. If not they dont*

- **all is actually not needed because its just default in every media queries so no need just**
```css
@media (max-width: 500px){

}
```
- If we want to do changes only for specific purposes(like when the page is printed, turn blue), we can do:
```css
/* turn all text to black in printing out */
@media print{
    color: black;
}
```

>**It looks like whatever we add after `@media` is a property or a situation/ a set of properties in which the changes will take place.**

- The media queries still go in to the **waterfall** pattern so when we add a specific style under that, it will be overflown.
```css
@media (max-width:300px){
    p{
        color: blue;
    }
}
p{
    color: white;
}
/* p will stay white */
```

### Orientation

- If we want to change some properties whenever we change orientation modes then:
```css
/* change background to red when landscape mode */
@media (orientation: landscape){
    background: red;
}
/* change color to green when portrait mode */
@media (orientation: portrait){
    color: green;
}
```

## Whoops that is all lol. Okay Out!