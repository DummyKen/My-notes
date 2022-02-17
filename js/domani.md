# WDF's Dom Manipulation Vid notes

## 14 DOM manipulation techniques

### Adding elements

Example:

```javascript
const body = document.body
body.append("Hello World"); //appended a string
body.appendChild("")
```

- with appendChild, we can only append elements like `divs,ps,spans...`
- only one element can be appended when using `appendChild`

Create elements to append/add to:

```javascript
const div = document.createElement('div');
//adding texts to elements
div.innerText = "Hello world";
div.textContent = "Hello World 2";

//then add it to the body
body.append(div);
body.appendChild(div);

```



 
