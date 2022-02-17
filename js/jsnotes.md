### Mosh's Javascipt Course Notes

Here we go 

---

*This video is very very short compared to other videos so I think Imma finish it up in maximum of two days and then maybe I can move on to docs and projects and get my feet dirty. __This is just another programming language to get my hands on so gonna be easy I hope.__

- JS used to be only available to run on browsers but not now, we can use it outside browsers with node.

- ES6(ecma script 6): *just a bunch of rules and specifications surrounding JS*
---

Wanna write JS in Browser>>> Browser tag > Inspect > Console > Write JS 
    (**there are JS engines in every browser so**)

- Just write some JS code(*'console.log('Hello')'*) and 'Enter':
```javascript
console.log('Hello World');
```
for printing.
```javascript
- alert('Woo')
```
for the pop-up alert window.

---

(__Downloaded Node__)

- code files in basics folder

- best practice: *add JS script to the end of the body section* 

- javascript comment:
```javascript
//This is a comment
```
- whatever we write in console will only be visible in console section.

- linking JS files in HTML:
```HTML
<script src="./index.js"></script>
```

### Running Javascript on Node
---

- Terminal >
```cmd
node index.js
```
will show the same output as in console.

- *__Node__ is a runtime environment that includes __Google's V8 JS engine__, useful for executing JS code.*

---

### Variables

Declaring a variable
- Before ES6:
```javascript
var name;
```
- After ES6:
```javascript
let name;
```
*Before assigning values to the variables, the initial value is '**undefined**'.*
- Initializing variables:
```javascript
let name = 'Ken';

Rules: 
//No Reserved Keyword
//Have to be meaningful
//Not start with a number
//No space or hyphen(-)
//Case sensitive
Typically carmelCase
```
- Best practice: declare variables one on each line

(Concepts are just like in every other programming languages I presume.)

---
### Constants

Declaring:
```javascript
const hourlyRate = 4;
```
- If we assign a constant a new value later, an error will occur.

---
### Types

- Types of values we can assign/use with variables.
---
- Primitives/Value types
    - String
    - Number
    - Boolean
    - undefined
    - null
---
Boolean declaration:
```javascript
permission = true/false;
```
Null declaration:
```javascript
selectedColor = null;
```
*for creating an empty space.*

---
### Static vs Dynamic Programming Languages

- In static languages(like C), we cannot change the type of the variables once set.
- In dynamic languages(like JS/Python), we can change them.
Example:
```javascript
name = 'Ken';
typeof name //string
name = 3;
typeof name //number
```
- JS doesn't have two types of numbers(float/int), just numbers.

---
## Reference Types

### Objects


Example:
```javascript
let color = null;
typeof color; //object
```

- Instead of creating multiple variables under the same belt(**name and age of a person**), we can define an object(*__person__*) for those primary variables.
- *Similar to Python dictionaries.*

Example:
```javascript
//In stead of 
let name = 'Ken';
let age = 19;

//We can define an object
let person = {
    name: 'Ken',
    age: 19
};
//name and age are called properties in this case

//very similar to python dictionaries
```
#### *Accessing Properties under objects*

- **Dot Notation**

Example:
```javascript
console.log(person.name);

person.name = 'Jeff';
```
- **Bracket Notation**  
*(Just like in Python)*

Example:
```javascript
console.log(person['age']);

person['age'] = 30;
```
---

### Arrays

Array syntax:
```javascript
let names = []; //empty array

let persons = ['John','James','Jack','Josh'];

let persons = [person1.name, person2.name];
```

- We can access specific element with indexes. 
```javascript
console.log(persons[0]);
```

- Adding elements in array using index:
```javascript
persons[2] = 'James';

//or we can add different type as well

persons[2] = 3;
```

- *Arrays are objects in JS.*
- We can use some built-in functions/properties for arrays with '**array.function**':
```javascript
console.log(persons.find()); //example

console.log(persons.length);
```
---

### Taking input using **prompt()**

- We can take input from the user using prompt method that will display a pop-up input requesting window.
```javascript
input = window.prompt('Hey! What is your name!');
```
### Functions

- Part of the referance types
- Functions are *functions* ofc xD.
Example(syntax):
```javascript
function greet(){
    console.log('Hello World');
}

function display(name,age){
    name = window.prompt('Your name?:') //will open up a pop-up window
    console.log("Your name:",name);
}
```
Recalling the function:
```javascript
function do(this,that){
    console.log('Do',this);
    console.log('Do',that);
}
//recall 'do' function
do('Dance for 10 mins','Be gay');
```
---

### Types of functions

- Function with no return(DIY)
Example:
```javascript
function greet(){
    console.log('Hello!');
}
```
- Function with return
Example:
```javascript
function sum(a,b){
    return a+b
}
```
We have to initialize this return value from the *function* to use it later.
Example:
```javascript
console.log('Sum:',sum(30+90));
// (or)
total = sum(90,87);
console.log(total);
```

## Mosh's vid ends here. Will move on to sequel vids lol

---
# Extra vids
## Arrays
Array []
- We can modify or add more elements to the arrays just like that:
```javascript
let arr = [1,2];
arr[2] = 4;
console.log(arr);//[1,2,4]
```
---
## Functions

---
## strings

---
## If else
Syntax:
```javascript
if(condition)
    statement
else(){
    statement1
    statement2
}
```
---
## Loops





