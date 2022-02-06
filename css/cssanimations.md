# Notes from Net Ninja's CSS animations playlist:

This is the first time I am taking a Net Ninja's course.
---
I am really excited for this one and will move on to **online tutorials**'s playlist later on. 

# Topics
- [Transforms](#Transforms)
- [Transitions](#Transitions)
- [Keyframes](#Keyframes)
- [Animation basics](#Basics)
- [Web Examples](#Examples)

Wait I need jQuery? Meh I will just stick to it and see.

## Transforms

I think I know how these works I guess. They are used to transform elements' coordinates or move them around I guess. Just use `transform:` and its available functions will appear. 
- translate() - Moves the element from one place to another.
  - translateX() - Moves along X-axis
  - translateY() - Moves along Y-axis(opposite Y-axis)

Example:
```css
img{
    transform: translate(200px, 100px)
    /* 200px on X-axis and 100px on Y-axis */
}
```
- scale() - changes the size to that px.(either shrink or spread/expand). 1 is default; anythin less than 1 is gonna shrink and anthin > 1 is gonna stretch. 
  - scaleX() - stretch/shrink along X-axis
  - scaleY() - stretch/shrink along Y-axis

Example:
```css
img{
    transform: scale(3);
    /* will make it thrice as big as original both X and Y */
    transform: scaleX(0.5);
    /* shrink it along the X-axis */
    transform: scaleY(4);
    /* stretch it along the Y-axis to fourth times the original */
    transform: scale(2,1); /*X,Y*/
    /* will twice the size on X-axis and Y-still the same */
}
```
- rotate() - rotate the element ofc
  - rotateX() and rotateY() are not really visible on the web page.
  - rotateZ() is much clearer visually.(it will tilt the element 360deg).
    - positive value --> clockwise
    - negative value --> anti-clockwise

Example:
```css
img{
    transform: rotateZ(45deg);
    /* 45deg clockwise */
    transform: rotateZ(-45deg);
    /* 45deg anti-clockwise */
}
```
- It is possible to do all these transformations altogether.
```css
img{
    transform: rotateZ(-90deg) translateY(200px) scale(2);
}
/* they will transform sequentially. */
/* in this case: rotateZ-->translateY-->scale */
```
---
## Transitions

I atleast know what they are and how they work basically. This changes the elements from one state to another.

v3 036
