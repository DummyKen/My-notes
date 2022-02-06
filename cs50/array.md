# Notes from CS50's Week2
## Arrays

*most boring topic in every programming language not gonna lie :)*

### Here we go

- Clang is the one we're using to compile files in CS50 ide.
>Using `clang` to compile c files
```
clang -o hello hello.c 
```
- means output the file `hello` with the input `hello.c`.
>Modified *added lcs50 to link to CS50*
```
clang -o hello hello.c -lcs50
```
### Steps in compiling our program
- Preprocessing
- Compiling
- Assembling
- Linking

What happens under the hood is just a mess lol ').

---
### Debugging with printf?? ')

Malan meant when trying to debug, its really helpful to use the **print** statement to help us find more about the errors/bugs. We can use the **print** statement to actually see where exactly or approximatey the error is happening.
- I am already doing all these.
---
## Debug50

- A tool used for debugging. Quite difficult to get used to Malan says.
- A debugger is a program that allows us to run code line by line and look inside of  variables and other pieces of memory inside the computer. The program is run much more slowly.

To use that:
```
debug50 ./file_name
```
- it might open up a GUI at the right side of the screen and we can use it to debug. I think I can dig that up for real.
- We have to set up a breakpoint to state where to pause execution of the program and debug.

*We can use both **step over** or **step in**(to step into a function other than main) in `debug50`.* 
- And it will jump to next interesting line in function(*like get_int function*) and it will be showed up in the `Call Stack` part of the debugger.
>Key takeaway here: Use a debugger, presumably `debug50`
---
### Rubber Duck Debugging

I kinda get where this is going to. This somehow utilizes the *`talk your problem out`* method, and in this technique, instead of talking to other humans, we talk to a rubber duck ") I think, or to an imaginary rubber duck or some sort of that. 

Yep, I was right. I can just talk to myself as I always do I guess. :)

---
Five minute break of the lecture and that I will call it a day as well.

---
Continuing on

### Another topic about memory :)

and boom

## Arrays

*I believe this wont even be a problem; but just a change of syntaxes.*
Declaring:
```c
int scores[3];
//data type/name/length
```
Adding values:
```c
scores[0] = 32;
scores[1] = 23;
scores[2] = 23;
```
Using loops to take inputs/arguments into the array:
```c
for(int i = 0;i < 3;i++)
{
    scores[i] = get_int("Score...");
}
```
We have to assign an array's length when declaring it.
- End of the 
string is denoted by `\0` called `null character`. And we can use this to print a string until we reach to the end. The same function named `strlen()` does the same thing by inserting the header file `string.h`.
- `C` has islower() as well.

### Taking input in `main` function
```c
#include <cs50.h>
#include <stdio.h>
#include <string.h>
int main(int argc, string argv[])
{
    if (argc == 2)
    {
        for(int i = 0,n = strlen(argv[1]); i < n;i++)
        {
            printf("%c\n", argv[1][i]);
        }
    }

}
```

---
# Welp that was it for week 2.