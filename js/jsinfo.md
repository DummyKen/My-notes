## JSInfo short notes and tips
### And topics
---
## [Strict Mode](https://javascript.info/strict-mode)
  - Using `use strict`  for modern functioning.
  - We have to add `use strict` at the very first tho.
  - Using `use strict` in a browser developer console
  ```javascript
  'use strict'; //<Shift+Enter for a new line>
  //...code..
  //<Enter to run>
  ```
  - In modern JS, `use strict` is auto enable so we dont have to add it personally. 
---
## [Variables](https://javascript.info/variables)
  - Already mastered ").
  - Keyword `let` to declare a variable.
  - *camelCase* is widely used for variable names.
  - **Case-sensitive** variable names.
  - `const` for constants.
  - Use **UPPERCASE** letters for the hardcoded variables(*whose values are already known before executing the program and directly attached to the code!*). Example:

```javascript
const BIRTHDAY = '17.01.2002'; //already known
```
---
## [Data Types](https://javascript.info/types)
- Here we go
- Dynamically typed so we can put in a numerical value inside a variable that once stored string.
- Special numeric values:
  - Infinity
  - -Infinity
  - NaN(*computational error/result of an incorrect or an undefined mathematical operation*)**not cool I guess ')**
    - Any further operation on `NaN` returns a `NaN`.
- Mathematical operations are safe. There will not be an ugly red error showing up even if we do smth totally stupid lol. At least it will give out the output as `NaN`.
- In JS, the 'number' type cannot represent int values larger than `((2^53 -1)(*9007199254740991*)` or less than `(-2^53 -1)`. 
- We do just fine with these limits but when we do crypytography or smth, we may need them to get bigger and that's where `BigInt` comes in.
- `BigInt` can represent numbers of arbitrary length. They are created by adding **n** at the end of the numbers. Example:
```javascript
const bigInt = 132238223832932832838928n;
//rarely used 
```
- single/double quotes/backticks(extended functionality quotes)
- Using ` ``s ` for extended functionality:
```javascript
let name = "Ken";
//embeding a variable
alert(`Hello! ${name}! Welcome.`); //Hello! Ken! Welcome.
//embeding an expression
alert(`The result is ${1+3}`); //The result is 4
```
*only applicable to backticks.*

- `null` does not belong to any types at all. This `null` doesnt represent/reference anything. It just means it's empty/nothing/value unknown. *We can use it when we don't know about the value of a variable at first but we might know later(and then we can just put the new value in there.*)Example:
```javascript
//at first we won't know the user's age so
let currentUserAge = null;
//then we'll ask the user to confirm their age and then we will grab that value and put it into the null
currentUserAge = someFunction();
```
- `undefined` means undefined nothing else. It serves as a default initial value for unassigned variables.
```javascript
let amountOfBreads;
console.log(amountOfBreads); //undefined
```
- The `object` type is special. And `symbol` type is used to create unique identifiers for objects.(*later*)

#### The `typeof` operator

- returns the type of the parameter
- *with or without parantheses*
```javascript
typeof undefined // "undefined"

typeof 0 // "number"

typeof 10n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"
```
Some different types:
```javascript
typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)
```
- `Math` is a built-in object.
- `typeof null` is an officially recognized error.
- `alert` is a function so function

### Summary
There are **8** basic data types in JS:
- `number` for any kind of numbers(limit: 2^53 - 1)
- `bigint` for arbitrary-length numbers.(*added n*)
- `string` for strings
- `boolean` 
- `null` for unknown values(empty socket)
- `undefined` for undefined values
- `object` for more complex data structures(objects)
- `symbol` for unique identifiers

Typeof: returns the type of variable.
- `typeof x` or `typeof (x)`
- returns a string(*"number"*, *"boolean"*)
---
## [Interaction: alert, prompt, confirm](https://javascript.info/alert-prompt-confirm)

### Alert 
- shows a message and waits for the user to press 'OK'
```javascript
alert("Hello");
```
*The mini-window with the pop-up is called a **modal** window. **The word "modal" means that the visitor can't interact with the rest of the page until they have dealt with the window. In this case, until they press "OK".*

### Prompt

- accepts two arguments:
```javascript
result = prompt(title, [default]);
// [default] is blank by default
```
- shows a modal window with a text message(*title*), an input field for the visitor, and the buttons OK/Cancel. 

>Example:

![Example prompt](https://static.javatpoint.com/javascriptpages/images/javascript-prompt-dialog-box3.png)

- User and enter some input in the input field(into `result` and we can make use of that later.)
- The call to `prompt` returns the text from the input field or `null` if the input was canceled.
```javascript
let age = prompt('How old are you?',100)
// 100 is the default value and will appear in the input textbox
alert('You are ${age} years old!');
//100 will be replaced by whatever the user types in
```

### Confirm

Syntax:
```javascript
result = confirm(question)
```
- shows a modal window with a `question` and two buttons: `OK` and `Cancel`.
- The `result` is `true` if OK is pressed and `false` otherwise.
```javascript
let isBoss = confirm("Are you the boss?");
// isBoss will true if OK is pressed and false otherwise
alert('Are you a boss?', isBoss);
```
>Example:
![Confirm Example](https://s1.o7planning.com/en/12271/images/34328848.png)

### Summary

- alert() | shows a message
- prompt() | shows a message asking the user to input text. It returns the text,or if cancel button or `Esc` is clicked, `null`. The input value can be stored in a variable
- confirm() | shows a message and waits for the user to press `OK` or `Cancel`. It returns `true` for `OK` and `false` for `Cancel|Esc`.
- **All these methods are modal: they pause script execution and does not allow the user to interact with the rest of the page until the window has been dismissed. **
- *There are two limitations shared by all the methods above:
  - The exact location of the modal window is determined by the browser(usually in the center).
  - The exact look of the window also depends on the browser. We can't modify it.*
---
## [Type Conversions](https://javascript.info/type-conversions)

*most of the time, operators and functions automatically convert the values given to them to the right type. But sometimes we might want/need to explicitly convert a value to the expected type.*

### String Conversion
- it happens when we need the string form of a value. Example:
```javascript
let value = 'true';
alert(typeof value); //boolean

value = String(value); //string conversion
alert(typeof value); //string
```
*I kinda think these are not very frequent and we use it only when we want to make sure the type of a variable is exactly what we want and the fact that type of teh variables get changed automatically is very cool*.

### Numerical Conversions

**Again, these conversions happen in mathematical functions and expressions automatically.**

Example:
```javascript
alert("6"/"3"); //3 | strings are converted to numbers automatically
```

---
## Basic Operators / Maths
- Unary = single operand operation
```javascript
let x = 13;
x = -x;
```
- Binary = two operands operation
```javascript
let x = 2;
let y = 3;
return x +y;
```
- Exponentiation is the same as Python `**`.
  - So we can find square root and other more roots using this expo operator.
```javascript
// sqrt of 23344
return 23344 ** 1/2;
```
- `+` will concantinate strings.
  - **If one of the operands is a string, the other one will get converted to string as well.**

- We can chain the assignment statements:
```javascript
let a,b,c;
a = b = c = 29+30;
console.log(a);//59
console.log(b);//59
console.log(c);//59
```
- We can increment in `C` style:
```javascript
let count = 2;
count++;
console.log(count);//3
```
Or even:
```javascript
let count = 34;
++count;
console.log(count);//35
```

### Rare but not extinct operators
- Bitwise Operators
   1. AND(&)
   2. OR(|)
   3. XOR(^)
   4. NOT(~)
   5. LEFT SHIFT(<<)
   6. RIGHT SHIFT(>>)
   7. ZERO-FILL RIGHT SHIFT(>>>)
- Comma operator

---
## Comparisons
- When comparing strings, JS compares them letter by letter and it comes down to `ASCII` code.
- When comparing two different types, JS will convert both to numbers. (*Exclude strict equality*)