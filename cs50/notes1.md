## CS50's Notes
---
## Here I go
---
## Most important aspects of good code
- __Correctness__
- __Design__
- __Style__

Now I am in C...

Most of the notes will be in my notebook but I may write it some code in here just to visually see it. 

Tools:

[CS50 IDE](https://ide.cs50.io)

Printing Out:
```C
#  include <stdio.h>

int main(void)
{
    printf("Hello World!");
}
```
---
Converting to machine code from source code is the task of a __compiler__.

Just in CS50, there is this function(library from CS50): 
```C
get_string("Prompt")
```
for getting string input from the user.

Complete syntax:
```C
string name = get_string("What's your name?);
```
-To put in the string value and print it out, we need to add ' *%s* ' as a placeholder for the string to come in. So:
```C
printf("Hello, %s",name);
```
where the string 'name' will take the place of the placeholder '%s'.

-To use the 'get_string' function, we have to import(#include) the CS50's library at the head of the program. The same with other libraries as well.
```C
#include <cs50.h>
```
- *Readability* - a good practice to even name the variables readable names.

-Moving the cursor to a new line everytime we compile:
```C
printf("Hello!\n");
```
will do the trick.

<!-- will move on to CSS(34:49) -->
In C(and maybe other programming languages), the program is executed from right to left so that is why we have to put the __assignment__ statements on the rightside of the code.

 *Header Files* - libraries?? Example: 
```C
#include <stdio.h>
#include <string.h>
#include <cs50.h>
```
- stdio.h(standard input/output header file)
- We have to add these header files sort of like libraries or modules for doing certain things.

- *Help50* : There's a useful tool provided by CS50 to help make the error messages more readable. To use it, run:
```C
help50 make hello
```
instead of 'make hello'. Very cute and handy.

- C comment:
```C
//this is a comment
```
- Try to make sense when writing comments.

- *Style50* : Yet another tool but this time for styling purposes. It will tell us the status of the program related to code design. 

- *Check50* : Another tool that will test the correctness of the problem. (The command will always be different per every problem set/lab.) 
---
### Command Line Interface(CLI)

We can run file commands inside the cs50 ide. *Linux commands*.

- Removing file:
```unix
rm filename
```
- Renaming file:
```unix
mv hello.c goodbye.c
```
Not really intuitive and readable is it? ')

- Making a new folder
```unix
mkdir folder
```
- Moving the file(inside folder) to the parent folder
```unix
mv hello.c ..
```
---
### Types

*Some types we gonna get across:*
```C
bool, long, int, string, char, float, double, char
```

- long >>> char/int
- double >>> float
---
*Some _printf_ format codes:*
```
%c = single character

%f = float number

%i = integer

%li = long (integer)
```
- Integers has got limits, and so we can use longs instead.

---
### Operators

- +, -, *, /, %

- When we use '*float*' for division result value, it is not efficient?
Example:
```C
int x = 1; int y = 2;
float z = x/y; //this returns 0.0000 instead of 0.5
```
- To fix this: We have to use ***Type Casting*** which converts the type of the variable.
Example:
```C
#include <stdio.h>
int x = 1; int y = 2;
//to get the correct answer
float z = (float)x / (float)y;
//(float) casted x and y into floating point numbers
```
- () casting.
---

### Synthetic Sugar

- A term to describe writing code that is synthetically more pleasing although having the same properties.

Example:
```C
//instead of 
count = count + 1;
//sugar
count += 1;
//or even more sugary
count ++; //just in C family tho
```
---
### Conditional Statements

Syntax:
```C
if (x < y)
{
    printf("x is less than y\n");
}
else
{
    printf("x is not less than y\n");
}
```

Else if:
```C
if (x < y)
{

}
else if (x > y)
{

}
else if (x == y){

}
```
Above code but more stylistic?:
```C
if (x < y)
{

}
else if (x > y)
{

}
else
{

}

```
### Chars

- We have to use ' 's for comparing or using only one character(*not string*).
- 'char' is the datatype for only *one* character.
```C
if (c == 'n'){}
//instead of 
if (c == "n"){}
```

- When asking for input signal, we can't use *string.lower()* like in Python. Instead we have to use 'or'.
- 'or' = '||'
```C
if (c == 'Y' || c == 'y')
{

}
```
---
### Loops

- A forever(infinite) loop in C(while loop)

```C
while (true)
{
    printf("Hello World\n");
}
```
- Finite while loop(with deadend)
```C
int i = 0;
while (i < 50)
{
    printf("This and that\n");
    i ++ ; 
    //need to increment the variable
}
```
#### For Loops

Example:(printing *Hello World* 50 times)
```C
for(int i = 0; i < 50; i++)
{
    printf("Hello World\n");
}
```
---
### Abrstraction

- A problem solving principle whereby we can simplify complicated details.

Functions -
Syntax:
```C
//A function(func_name) that takes a number and print meow for that number of times
//Syntax: 
//return_type name(parameters)
void func_name(int)
{
    for(i=0;i<3;i++)
    {
        printf("Boo\n");
    }
}

//calling the function

```
*When we define a custom function before **main**, it is not very efficient. But other way around when we do it after **main** and decide to call it in **main**, it wont work either. So, we have to add the first line of the function declaration above **main**.

Example:
```C
void func_name(int);
int main(void)
{
    func_name(n);
}
```
---
### Checking input

> Do while loops ofc ").(my beloved friend)

- do{something} while{something is not right}(once the condition is *True*, *do loop* ends)

### Nested loops

---

```C
printf(".10%f\n",x/y);
//for printing 10 decimal values of the floating point
```

YO! Done the 'C' vid lol.

Onto the pset 01 and lab01?

