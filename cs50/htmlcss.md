# Notes from CS50w's Week0 lecture: HTML & CSS
(I think there will be also Bootstrap and Sass)

I really needed a refresher on all these topics. What better lecture to watch. 

**There's also notes available**. So I wont be writing down a ton of notes.

Style Precedence(strongest to weakest):
1. inline
2. id
3. class
4. type

## Responsive Design
### Viewport
  - visual part of the screen user sees
  - there's is a short line(which comes in default per emmet boilerplate) that makes sure the viewport is compatible with that of the device's width.
### Media queries
Note: We can hide/show content by using `display` property.
### Flexbox
My arched nemesis :). Wrapped elements.
- `Flex-wrap: wrap;` to wrap around the elements.

### Grid
- `grid-column-gap` - gap between columns
- `grid-row-gap` - gap between rows

## Bootstrap
We can just apply some
- Just copy the `cdn` link into the css/html
- This will default add some custom styles to tags and we can apply to certain divs only as well.
- Or maybe I can add custom styles to those bootstrap styling as well.
- Needs to be online tho.
---
### Sass
- For faster and remove repetition.
- Can use variables
- Uses `.scss` file extension

In:
`scss.html & variables.scss`
- Setting a variable in Sass:
```css
$color: red;
```
- Using the assigned value into properties:
```css
ul{
  font-size: 14px;
  color: $color;
}
ol{
  font-size: 18px;
  color: $color;
}
```
- When connecting to html as a css, we can't just link it like a css file. We need to *compile/translate* scss to css.
- Compiling:
  - Download Sass
  - `sass filename.scss:filename.css`
  - Then just link to the `css file`
- We need to compile the scss file everytime after we make changes to the file.
- To automate that process, we can do(although I cant)
```sass --watch filename.scss:filename.css/directory```

---
### Nesting with Sass
```css
div{
  font-weight bold
  ul{
    
    li{
      color: grey;
      font-size: 10px;
    }
  }
}
```
---
### Inheritance with Sass
Eg: this `class` will be the same as that `div` but different background colors. And the other two classes will also be just like that `div` but again different colors for each.

>Example :*Three message divs with the same `message` properties but different background colors per their classes.*
```scss
%message {
   font-size: 18px;
   border: 1px solid black;
   padding: 20px;
   margin: 20px:
}
/* for success message */
.success{
  @extend %message
  background-color: green;
  
}
/* warning message */
.warning{
  @extend %message
  background-color: yellow;
}
// error message
.error{
  @extend %message
  background-color: red;
}
```

### And boom we are done with W0 lecture.