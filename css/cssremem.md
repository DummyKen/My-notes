## Notes from Brad's CSS Units vid
I still cant wrap my head around these.

### `Rem`
>`1 rem` = default font size of browser(mostly 16px)
- `rem` is always relative to the root <html> element.
  - So if we or users change the font-size of their browser, the `rem` font-size will also be changed accordingly.
- `1 rem` is the default `16px` font-size on browsers. Or whatever px the font-size of the browser it's run on. 
- This is very cool coz this will automatically make sure the text visibility and such.
- We can use `rem` not only on font-size but other as well like paddings, widths?, borders.(decimal may come).
---
### `em`
- While `rem` is relative to the root(<html>)element,`em` is actually relative to its parent element. Example:
```css
/* box > p */
.box{
    font-size: 30px;
}
p{
    font-size: 1rem;
    border: 0.1rem black solid;
    padding: 1rem;
}
```
>Adding `rem` like this will not change the font size at all as it is relative to the root html. But:
```css
p{
    font-size: 1em;
    border: 0.1em black solid;
    padding: 1em;

}
```
will actually increase the font size and padding to 30px and border to 3px.
- If there is no parent element, `em` will just work the same as `rem` and be relative to html element.
---
### `vh`
- Relative to browser's height.
- `1 vh` = 1 % of browser's height(viewport height)
  - `50 vh` = half of browser's height(viewport height)
- This will come in really handy when we want the background to always fill up the browser's height no matter what.
---
### `vw`
- Same as `vh` but width.
- NOT used so often.
- `1 vw` = 1 % of browser's width(viewport width)

---
Done~

Now this was not really tricky, was it? They really made it tricky.

TODO:review me


