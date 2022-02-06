## Notes from Traversy's Sass crash course

### Here we go

- Sass(Syntactially Awesome StyleSheets)
- CSS PreProcessor/Extension
- Additional features(not in CSS)
- Has to compile *.scss* files in CSS files(*needs a compiler*)
- Transforms CSS into almost a programming language
---

### Two ways of Sass

1. .scss
2. .sass

---
# Advantages of Sass over CSS

### Variables in CSS into Sass

- Prefixed with a *'$'*
Example:
```css
$primary-color: gray;
```
---
### Nesting

- One of the core reasons of using Sass.
Example:
```css
nav{
    ul{
        margin: 0;
        padding: 0;
    }
    li{
        display: inline-block;
    }
    a{
        color: black;
    }
}
```
---
### Modules

- We can combine all the *scss* files into one big file for better accessability.
---  
### Mixins and Functions
---
### Inheritance
>Using `@extend` property, we can just copy one element's properties into another one and modify that later one. Example:
```scss
#message {
    border: 1px solid #ccc;
    padding: 10px;
    color: #333;
}
#error-message{
    @extend #message;
    border-color: red;
}
#success-message{
    @extend #message;
    border-color: green;
}

```
---
### Operators
---
### Conditionals
---

## Jumping in ---


