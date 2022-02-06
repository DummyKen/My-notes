## Notes from Traversy's JS crash course

### Here we go

### Intro
- A multi-paradigm language(OOP,...)
- Just my observation:
Javascript if..else.. statements
```javascript
if(sum == 0){
    console.log('Erorr');
}
else{
    console.log('OK');
}
```
---
### Console

- A bunch of console methods(functions):
```javascript
//error message
console.error('This is an error'); 
//warning
console.warn('This is a warning');
//clear
console.clear();
```
---

### Variables

- let/const
- *let* is modifiable but *const* is not.
**Tip: always use *'const'* unless we will reassign it later on.**

---
### Data Types

- Primitive(Direct to memory[not a reference])
  - string (*'Ken'*)
  - boolean (*true/false*)
  - numbers (*3*)
  - null (empty)
  - undefined (*let z:--undefined*)
**We can use *typeof()* to find out the type.

---
### Template Strings(literals)

> Used instead of concatenation
- Kind of like formatted strings in Python but different syntax:

Example:
```javascript
name = 'Ken';
age = 20;
console.log(`My name is ${name} and I am ${age}.`);
//pretty cool stuff
```
----
### Some string methods

- string's length
```javascript
s = 'thistah'
console.log(s.length);
```
- uppercase/lowercase
```javascript
console.log(s.toUpperCase());

console.log(s.toLowerCase());
```

- string slicing(*taking out substring*)
- *the same as Python, **up to but not including***
```javascript
//.substring(start_index, b4_index)
const s = "Hello World";
console.log(s.substring(0,7)); //from 0 to 6(not 7)
//Hello W

//combined
console.log(s.substring(0,7).toUpperCase())
//HELLO W
```
- split the string into array
```javascript
console.log(s.split('')) //default
```
> *the same as python*
---
### Arrays

> variables that hold multiple values (*just like lists*)

Example:
```javascript
const fruits = ['apples','oranges','bananas',3,true];
```
- In arrays(**JS**), we can have elements of different types together as well. (*strings,booleans,*)
- No sub-arrays tho.

Accessing the array elements:
```javascript
console.log(fruits[0]);
```

Adding an element at the end of the array:
```javascript
fruits.push('mangos');
```
Adding an element at the start of the array:
```javascript
fruits.unshift('guavas');
```
Finding the index of a certain character:
```javascript
fruits.indexOf('strawberries');
```

*Sometimes I wonder JS is just very similar to Python with **'of'** added at the end. :)*

---
### Object Literals(Objects)

#### (*Python dictinaries ripoff*)

- Key-value pairs(just like python dictionaries)
Example:
```javascript
const person={
  firstName: 'Ken',
  lastName: 'V',
  age: 19,
  single: true
}
```
- We can add 'arrays' in it too.
- And sub-objects too.
```javascript
const info={
  job: 'Gay',
  addrress: {
    street: 'gay st',
    city: 'gay city',
    state: 'gay state'
  }
};
//Accessing the sub values of the sub-objects:
console.log(info.address.city); //gay city
```

- Pulling elements out of the object:

```javascript
const person={
  firstName: 'Ken',
  lastName: 'V',
  age: 19,
  single: true,
  address{
    street: 'Gay st',
    city: 'gay city'
  }

};
const {firstName, lastName, address: { city }} = person;
//firstName and lastName address().city)inside the person are now variables each.
```
- Adding properties to the object.

```javascript
person.email = 'banyarnaingcodes@gmail.com';
console.log(person) //email included
```

### Arrays of Objects

```javascript
const todos = [
{
  id: 1,
  text: 'Take out trash',
  isCompleted: true
},
{
  id: 2,
  text: 'Meeting with boss',
  isCompleted: true
},
{
  id: 3,
  text: 'Dentist Appt',
  isCompleted: false
}
];

//grabbing items from above array of objects

console.log(todos[2].text);
//Dentist Appt
```
---

### Json?

- Been trying to learn this one
- Similar to object literals(*formatted strings*)
- Just copy and paste it into json formatter and boom.

If we want to convert to json inside our script:
```javascript
JSON.stringify(array_name);
```
Example:
```javascript
const todos= [.....smth....];
const todoJSON = JSON.stringify(todos);
console.log(todoJSON);
```
---

### Loops!

> **For** loops

```javascript
for(let i = 0; i < 10; i++){
  console.log(i);
}
//0 --> 9
```
*the same as C*

> **While** loops

- We set the variable outside of the loop.

Example:
```javascript
let i = 0;
while(i<10){
  console.log(`For Loop No.${i}`);
  i++;
}
```

> **For of** loops
**(the same as python's *in* operator)**
```javascript
//basically the same as python's in 
//for i in todos
for(let i of todos){
  console.log(i.id);
}
```
---
### High ordered array methods

> forEach

- this takes in a function as a variable to be used in the loop.

Example:
```javascript
//i is just a variable but has to be passed in as a function lol
todos.forEach(function(i){
  console.log(i.text);
})
```
*these look much better with arrow functions.*

> map

- takes in a function variable and **returns** an *array*. 
- similar format as *forEach*

```javascript
const todoText = todos.map(function(i){
  return i.text;
});
//will return a related array.
```

> filter

- also returns an array 
- maybe we use it to filter out certain results?

```javascript
const todoCompleted = todos.filter(function(i){
  return i.isCompleted === true;
}); //return only the ones with value 'true'
console.log(todoCompleted);
//will return an array
```
---
### Conditionals
I've already mastered lol.
Stuff like `|| && if,else,else if`

### Ternary Operator(`?`)
If one condition is true, this else,that. Sort of like shortened if/else chain.
```javascript
const x = 10;
const color = x > 10 ?'red':'blue';

console.log(color);//blue in this case
//color = red if x >10 and blue if x <10
//blue in this case
```
### Switch/case statements
I have mastered these:
```javascript
switch(color){
  case 'red':
    console.log("It's red");
    break;
  case 'blue':
    console.log("It's blue");
    break;
  // when none of the statements get matched
  default:
    console.log("It's neither red nor blue");
    break;

}
```
---
## Functions
Just like functions in every other languages
```javascript
//a function that will add numbers
function addNums(num1,num2){
  console.log("The Sum",num1+num2);
  return num1*num2;
}
addNums(12,9);//21
console.log("Product:",addNums(2,90));//180
```
---
## Arrow Functions
When we wanna use a function as an arrow function, we assign that as a variable and not a function. 
```javascript
const addNums = (num1 = 1, num2 = 1) => {
  return num1 + num2;
}
console.log(addNums(5,20));//25
```
```javascript
const addNums = (num1 = 1,num2 = 1) => num1+num2;
console.log(addNums(23,4));//27
// we dont need the `()` if there is only one statement
```
---
### Lexical `this`
Too advanced for this crash course?
---
## Object-oriented JavaScript
>Very similar to Papa Python:

- Using constructor function:
```javascript
function Person(firstName, lastName, dob, age){
  // we use `this` to assign each to respetives
  this.firstName = firstName;
  this.lastName = lastName;
  this.dob = dob;
  this.age = age;
}

//Instantiate object
const person1 = new Person('Ken','V','Jan 17,2002',20);
console.log(person1);//{'firstName':'Ken',lastName:'V',dob:'Jan17,2002',age:20}
const person2 = new Person('Brad','Vera','Jan 1,2022',30);
console.log(person2);//{firstName:'Brad',lastName:'Vera',dob:'Jan 1,2022',age:30}
```
- We can add methods/functions to these objects as well.
```javascript
//adding new method to that Person object
this.getBirthYear = function(){
  return this.dob.getFullYear();
}
console.log(person1.getBirthYear());//2022
```
---
## Dates
```javascript
const today = new Date('15-1-2022');//will turn the date into a full date format.
```
Date object has a lot of functions built-in.
```javascript
console.log(today.getFullYear());//2022
```

---
And that wraps the ES5 OOP without classes.

---
### ES6 classes
>Synthetic sugary stuff
```javascript
class Person{
  constructor{firstName,lastName,dob}{
    this.firstName = firstName,
    this.lastName = lastName,
    this.dob = new Date(dob);
  }
  getBirthYear(){
    return this.dob.getFullYear();
  }
  getFullName(){
    return `${this.firstName} ${this.lastName}`;
  }

}
```
>And that wraps up the JS OOP for now.
---
## DOM(Document Object Manipulation??)
I will just watch the DOM crash course of Brad later on. I dont want to go and copy a bunch of crap so yeah later on.
- I think its just a bunch of like `document.getsomething something`

>grabbing only one unique element from the document
```javascript
console.log(document.getElementById('my-form'));
//<form id="my-form"></form>
```
---
>query Selector
```javascript
console.log(document.querySelector('.container'));
//<h1>JS Crash</h1>
```
>querySelectorAll
```javascript
console.log(document.querySelectorAll('.item'));
//will return every thing with that class in an array style
```
>getElementsByClassName

the same as query selector but inferior?

---
### Manipulating the `DOM`
Examples:
```javascript
const ul = document.querySelector('.item');

//methods
ul.lastElementChild.remove();
ul.firstElementChild.textContent = 'Hello';//changed the text
//second child element
ul.children[1].innerText = 'Brad';
ul.lastElementChild.innerHTML = '<h1>Hello</h1>';

// styles inside JS
const btn = document.querySelector('.btn');
btn.style.background = 'red';
```
---
## Events
```javascript
const btn = document.querySelector('.btn');
btn.addEventListener('click', (e) => {
  e.preventDefault();
  console.log('click');
});

//the info of the event's
console.log(e.target.id);
```
>Yea, the rest in DOM crash course.

---

### And Boom this one is donezo.
---

