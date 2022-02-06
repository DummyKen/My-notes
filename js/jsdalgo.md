# Notes from FreeCodeCamp's JS DS & Algo

 I dont think I will be taking a lot of notes.
 In JS, all these are possible:
 ```javascript
 a += 29;
 b -= 3;
 c *= 4;
 d /= 23;
 ```
 and maybe in Python too; I just never tried it yet.

 ### Escaping Quotes in Strings

 To display `'`,`"`,` `` `s just the way they are in strings and not mess them up:
 ```javascript
 print("\'Hey What\'\s up!\', he greeted.");
 //'Hey What's up!', he greeted.
 ```
 ---
 - Single and double quotes work the same in JS.
 - Escaping characters using `\`s.
```
Code	Output
\'	single quote
\"	double quote
\\	backslash
\n	newline
\r	carriage return
\t	tab
\b	word boundary
\f	form feed
```
Example:
```javascript
const myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
/*FirstLine
    \SecondLine
ThirdLine
*/
```
- We can add strings to strings using `+=` just like we do with numbers.
```javascript
let myStr = "I come first. ";
myStr += "I come second.";
document.write(myStr); //I come first. I come second.
```
- Just like appending strings to strings, we can append variables into strings as well(or another variables)
```javascript
const anadjective = "coolest!";
let myStr = "Ken is the";
myStr += anadjective;
//Ken is the coolest!
```

### Finding the length of the string using `.length`

```javascript
const mystring = "This is a string."
console.log(mystring.length); //13
```

- Just like in Python, we can fetch characters at certain index in a string using `[]`.
```javascript
let firstName = "Banyar";
let firstChar = firstName[2]; //n
```

### String Immutability

In JS, `String` values are **immutable**.
```javascript
let myStr = "Bobby";
myStr[0] = "K"; //error
```
But the whole `String` itself is mutable tho.

- Getting the last character of the string using bracket notation:
```javascript
let myStr = "Bobby";
let lastChar = myStr[myStr.length - 1]; //get it :)
```

- Use Bracket Notation to Find the Nth-to-Last Character in a String
```javascript
let myStr = "Bobby";
let thirdToLastLetter = myStr[myStr.length - 3]; //b
let fourthToLastLetter = myStr[myStr.length - 4]; //o
```
Pretty useful I'd say

### Arrays

Yeah. Syntax:
```javascript
const sandwich = ['peanut better', 'jelly','bread'];
console.log(sandwich[2])//bread
```
One thing is that `JS strings` can contain elements of different kinds as well. I dont know where they are used but yeah:
```javascript 
const items = ['Clock', 'Umbrella', true, 34];
//no error lol
```

### Nesting arrays

We can nest arrays inside arrays as well.
```javascript
const teams = [["Bulls",23], ["Cows",30]];
//maybe to associate the related items together

console.log(teams[0][1]); //23
```

### Manipulate Arrays with push()

`.push()` takes one or more parameters and appends them at the end of the array.
```javascript
const arr1 = [1,2,3,4];
arr1.push(7); //[1,2,3,4,7]
const arr2 = ["Boo","haha","lol"];
arr2.push(["Yoo","Hey"]); //["Boo","haha","lol",["Yoo","Hey"]]
```
### Manipulate Arrays with pop()
`.pop()` pops out the last value of the array(*just like in python*). We can put the `popped` value into another `variable`.
```javascript
const arr1 = [1,2,3,4];
const lastvalue = arr1.pop();
console.log(arr1);//[1,2,3]
console.log(lastvalue)//4
```
### Manipulate Arrays with shift()
`.shift` removes the first element of the array:(*just like pop but reverse*)
```javascript
const arr1 = [1,2,3,4];
const first = arr1.shift();
console.log(arr1); //[2,3,4]
console.log(first);//1
```
### Manipulate Arrays with unshift()
`.unshift()` works the same as `.push()` but reversed; it adds to the first element of the array.
```javascript
const arr1 = [1,2,3,4];
arr1.unshift("Kiki");
console.log(arr1); //["Kiki",1,2,3,4]
```

## Write Reusable JS with functions(JS functions)
Syntax:
```javascript
function functionName(){
    console.log("Hello World");
}
```
Recall the function:
```javascript
functionName();
```
Function with `arguments`:
```javascript
function greet(first,second){
    console.log(first,second);
}
//passing args
greet("Hello","Gay!");//Hello Gay!
```
Return value from function:
```javascript
function muliply(num1,num2){
    return num1*num2;
}
//put the return value into a `variable`
const product = multiply(12,323);//3876
```
### Global Scope and Functions

- When we declare variables without `let` or `const`, that will become a global variable.
- Scope is pretty much very simple, there is nothing out of the function related to the variables inside the function.
- **It is possible to have both local and global variables with the same name. In this case, the `local` will take precedence over `global`.**
```javascript
const someVar = "Cool";
function display(){
    const someVar = "Ugly as shat";
    console.log(someVar); //Ugly as shat
}
```

### Fetchin value from a no-return function
When we grab a value from a function with no return statement(*error or smth*), the function will by default return `undefined`.
```javascript
let sum = 0;
function findsum(Num){
    sum = sum+Num;
}
const finalSum = findsum(8);//undefined
```

- In JS, we can compare the number and string with the same value as it will just convert vice versa by itself. Example:
```javascript
1 == 1; //true
1 == "1"; //true
3 == "3"; //true
```

- Using strict equality Operator will return `true` only if the compared values have the same type as well.
```javascript
1 == "1"; //true

1 === "1"; //false
```

- Inequality operator:
```javascript
1 != 2 //true
1 != 1 //false
```
This is not strict and will use type conversion:
```javascript
1 != '1' //false
```

- Strict inequality operator:
```javascript
3 !== 3 //false
3 !== '3' //true
```
this will not use type conversion.

- `Greater than` operator(*also uses type conversion*)
```javascript
5 > 3 //true
4 > '2' //true
5 > '5' //false
'2' > 4 //false
```
- `Greater than or equal to` operator(*type conversion*)
```javascript
5 >= 5 //true
4 >= '2' //true
```
- `Less than` operator(*type conversion*)
```javascript
4 < 3 //false
2 < '9' //true
```
- `Less than or equal to` operator(*type conversion*)
```javascript
3 <= '4' //true
'5' <= 2 //false
```
#### Logical operators

- And `&&` operator
```javascript
if (num > 5 && num < 10){
    return "Yes";
}
return "No";
```
will return "Yes" if only num > 5 and num <10.

- Or `||` operator
```javascript
if (num < 5 || num > 10){
    return "NO";
}
return "Yep";
//will return "NO" once one condition is false
```

#### If/Else
```javascript
if(num > 20){
    return "Greater";
}
else{
    return "Lesser";
}
```
#### Else if
```javascript
if(num > 20){
    return "Greater than 20";
}
else if(num < 20 && num > 10){
    return "Between 10 and 20";
}
else{
    return "Less than 10";
}
```

### Switch statement
> Uses when there are multiple options/cases to choose from:
> Case values are tested with strict equality `===` operator:
Syntax:
```javascript
switch(value){
    case"a":
        console.log("A");
        break;
    case"b":
        console.log("B");
        break;
}
//this will change value from a to A or b to B
```
Example:
```javascript
function caseInSwitch(val) {
  let answer = "";
  // Only change code below this line
  switch(val){
    case 1:
      answer = 'alpha';
      break;
    case 2:
      answer = 'beta';
      break;
    case 3:
      answer = 'gamma';
      break;
    case 4:
      answer = 'delta';
      break;
  }
```
This is testing `val`'s value and changing the value of `answer` based on its value.

>Adding a default statement in Switch statements(*the same meaning as the last else statement in if/else statements*)
```javascript
function caseInSwitch(val) {
  let answer = "";
  // Only change code below this line
  switch(val){
    case 1:
        answer = 'alpha';
        break;
    case 2:
        answer = 'beta';
        break;
    default:
        answer = answer;
        break;
```
- If the `break` statement is omitted from a `switch` statement's case, all the following `case` statement(s) are executed until a `break` is found. So, we can have mulitple inputs with the same output group together with no `break` inbetween them.
```javascript
switch(val){
    case 1:
    case 2:
    case 3:
        result = "1, 2, or 3";
        break;
    case 4:
        result = "4 alone";
}
//case 1,2,3 will produce the same output.
```
- *When there are many options to choose from, a `switch` statement is more relevant than using a bunch of `if/else` statements.

### Return Boolean values from functions
```javascript
if(a===b){
    return true;
} else{
    return false;
}
```
A better way to do the above statement():
```javascript
return a===b;
//this will also return true or false
```

### Return Early Pattern for Functions
When a `return` statement is reached, the execution of the current function stops and control returns to the calling location(statement) and skips whatever statement after the `return` statement.
```javascript
function myFun(){
    console.log("Hello");
    return "World";
    console.log("byebye");
}
myFun();
//myFun() will stop executing after it logs "Hello", returns "World" and "byebye" will never be executed.
```
---
### Javascript Objects
*just like python dictionaries huh but a bit tricky as the name implies*
- Key-value pairs
- **Keys are called properties in JS.**

Example syntax:
```javascript
const dog={
    "name":"Whimpet",
    "legs":4,
    "tails":1,
    "enemies":["Water","Dogs"]
};
```
We can even omit the single-word string properties and the properties can also be numbers as well. Alternating syntax:
```javascript
const sample={
    make:"Ford",
    5:"five",
    "model":"focus"
};
//5 will be typecasted into string type
```
*If our object has any non-string properties, JS will automatically typecase them as `strings`.*

### Accessing JS objects properties with `Dot` Notation
There are two ways to access the properties of an object:
- using `.`
- using `[]`
They are the same.
```javascript
const myObj = {
    prop1:"val1",
    prop2:"val2"
};
const prop1val1 = myObj.prop1;
const prop2val2 = myObj.prop2;
```
*Note:*If the property of the project has a space in its name, we will have to use bracket notation.
```javascript
const myObj = {
    "First Name":"Ken",
    "Last Name":"V",
}
const firstname = myObj["First Name"];
const lastname = myObj["Last Name"];
```
We can use variables to look up for properties in objects.

### Updating Object Properties
```javascript
const myDog = {
    name:"Dodo",
    age:3,
    color:grey
};
myDog.name = "Maxim";//Dodo-->Maxim
```
### Adding new properties to Objects
Just add with the assignment statements.
```javascript
const myObj = {
    "First Name":"Ken",
    "Last Name":"V",
}
myObj.age = 19;
//now it's in
```
### Deleting object properties
```javascript
const myObj = {
    "First Name":"Ken",
    "Last Name":"V",
}
delete myObj["First Name"];
//now its long gone :)
```

## Using objects for lookups
Objects can be thought as key/value storage just like dictionaries. We can use `objects` to look up for tabular data rather than using `switch` or `if/else` statement chain.
```javascript
const alpha={
    1:"Z",
    2:"Y",
    3:"X",
    4:"W",
    ...
    24:"C",
    25:"B",
    26:"A"
};
//then we can just access by
alpha[2];
alpha[24];
```
## Testing objects for properties
We can use objects built-in method called `.hasOwnProperty(propname)` to determine that the `propname` property exists or not in that certain object. Example:
```javascript
const myObj = {
    "First Name":"Ken",
    "Last Name":"V",
}
myObj.hasOwnProperty("First Name");//true
myObj.hasOwnProperty(age);//false
```
It returns `true` or `false`.

- We can add arrays of strings or even objects into objects:
```javascript
const myObj={
    aliases:[
        "Ken",
        "V",
        "Banyar"
    ],
    age:19
}
```
- Or we can add objects into array:
```javascript
const ourMusic = [
    {
        artist:"Ken",
        title:"tittyboomer",
        formats:[
            "CD",
            "Radio",
            "LP"
        ],
        gold:true
    },
    {

    }
];
```
In this case, ourMusic is an array of objects.

### Accessing nested objects
We can access the properties of object inside the object by chaining together the dot or bracket notation:
```javascript
const ourStorage = {
    "desk":{
        "drawer":"stapler"
    },
    "bottom drawer":"soda"    
};
ourStorage.desk.drawer;//stapler
ourStorage["bottom drawer"];//soda
```
### Accessing nested Arrays
We can access the nested arrays by using bracket notations just like Python.
```javascript
const ourPets = [
    {
        animalType:"cat",
        names:[
            "Meowzer",
            "Fluffy",
            "Kit-cat"
        ]
    },
    {
        animalType:"dog",
        names:[
            "Chuck",
            "Guts"
        ]
    }
];
ourPets[0].names[2]//Kit-cat
ourPets[1].names[0]//Chuck
```
>And I did that `Record Collection thing`: I wrote exactly like the official solution and it did not work until I straight up copied the original. The code:
```javascript
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  if (prop !== 'tracks' && value !== "") {
    records[id][prop] = value;
  } else if (prop === "tracks" && records[id].hasOwnProperty("tracks") === false) {
    records[id][prop] = [value];
  } else if (prop === "tracks" && value !== "") {
    records[id][prop].push(value);
  } else if (value === "") {
    delete records[id][prop];
  }
  return records;
}
updateRecords(recordCollection, 5439, 'artist', 'ABBA');
```
---
## Loops
### While Loops
Syntax:
```javascript
const ourArray=[];
let i = 0;

while(i<5){
    ourArray.push(i);
    i++;
}
//1,2,3,4 will be added to ourArray
```
### For Loops
Syntax(*similar to C*):
```javascript
const ourArray=[];
for(let i = 0;i < 5;i++){
    ourArray.push(i);
}
//ourArray = [0,1,2,3,4]
```
We can change it to just add odd numbers by changing some expressions:
```javascript
const ourArray=[];
for(let i = 1;i < 10; i+=2){
    ourArray.push(i);
}
// ourArray = [1,3,5,7,9]
```
We can change it to go backwards as well.
```javascript
const ourArray=[];
for(let i = 9;i > 0; i-=2){
    ourArray.push(i);
}
// ourArray = [9,7,5,3,1]
```
Iteratating through an array with a `for` loop:
```javascript
const arr = [9,7,5,3,1];
for(let i=0;i<arr.length;i++){
    console.log(arr[i]);
}
//9 7 5 3 1 in order will be logged
```
#### Nesting For loops
We can use nested for loops to access inside a multi-dimensional array:
```javascript
const arr = [
    [1,2],[3,4],[5,6]
]
for(let i=0;i<arr.length;i++){
    for(let j=0;j<arr[i].length;j++){
        console.log(arr[i][j]);
    }
}
//1 2 3 4 5 6 in order will be logged
```
### Do...While Loops
>Do [....] while true. Once false, stop the loop.
```javascript
const myArray = [];
let i = 0;
do{
    myArray.push(i);
    i++;
} while(i<5);
//as long as i<5, i will be added to myArray. Once i = 5, the loop will stop
```
*The difference between other loops and `do..while` loops is that `dowhile` loops will always make sure the statements inside the loop will be run at least once even when the condition is not true.
