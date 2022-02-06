## Mosh's Python Course

Won't be difficult at all I guess as I am doing this just for warming up my Pythonista skills. 

--- 
- Wow, we can write this to print out the same thing multiple times:
```python
print('Yes' * 10)
```
will print 'Yes' 10 times(consecutively).

---

### Variables

Again easy peazy.

---
### Strings

- Has to be 
```python
"This 'that' "
'This "that" '
'''This 
    That 
    Thatt
'''
```

- [index] to access a specific character
- [1st:last] to access specific characters(up to not including)

---
### Formatted Strings

- example:
```python
first = 'Ken'
last = 'V'
msg = f'{first} [{last}] is a coder'
```
where the variables will fill up the '{placeholder}' s. This is much more simpler than concatinating strings.

---
### Arithmetic operations

- '//' results in 'int' tho
---
### Opeator Precedence

- Duh duh

- 'xx' and '/' >> '+','-'
- () >> everything 
---

### Math Functions

- round() function
```python
round(2.9) #3(rounded value)
```
- abs() function
```python
abs(-2.8) #2.8(absolute value)
```

 **To use complex math functions, we need to import the *'math'* module.**
```python
import math

#recalling and utilizing math functions
math.ceil(2.3)
math.floor(2.9)
```
*We can refer to the documentation for the rest.*

---
### If Else Statements 

- Already mastered ')
--- 

### Logical Operators

- I think I know this well. 
- '*NOT*' is new tho.
---
### Comparison Operators

- Already mastered :')
---
### While loops

- Printing out strings for a number of times: *when a string is multiplied by an integer, it will be displayed that number of times.
example:
```python
k = 1
i = 5
while k <= 6:
    print('$'*k)
    k += 1
while i > 0:
    print('$'*i)
    i -= 1
print('Boop')

#result k = 1
i = 5
while k <= 6:
    print('$'*k)
    k += 1
while i > 0:
    print('$'*i)
    i -= 1
print('Boop')
#Result:
# $
# $$
# $$$
# $$$$
# $$$$$
# $$$$$$
# $$$$$
# $$$$
# $$$
# $$
# $
# Boop
```
---
### Small guessing game using 'while' loops :)

> A number guessing game where you have to guess the key number. Your max attempt is '3'.

Code:
```python
key = 7
#attempts list
attempts = list()
guess_count = 0
while guess_count < 3:
    guess = int(input('Guess the number: '))
    attempts.append(guess)
    guess_count += 1
    if guess == key:
        print('You Win!')
        break
    if guess_count == 3:
        print("Nope! Attempt max exceeded!")
        break
print("Your total attempts: ", guess_count)
print("Your guesses: ", attempts)
```    
- *Weewoo*. We can add an '*else*' block to while loops as well!

Example:
```python
while i < 3:
    print('this')
#when something exceeds the while loops limits
else:
    print('Done')
```
---
### A small car game using while loops?

> A simulation game where the user can start,stop the car or quit.

Code:
```python
print('Welcome to my small simulation game!')
print('You can enter help to get some info about the game.')
engine_on = False
while True:
    command = input('>').lower()
    if command == 'help':
        print('''
For now, only 3 commands are available:
start = start the car
stop = stop the car
quit = quit the game:

    ~Have Fun~''')
    elif command == 'start':
        if not engine_on:
            print('Poopoo! Car started.')
            engine_on = True
        else:
            print('Car is already started.')
    elif command == 'stop':
        if engine_on:
            print('Buzamm! Car stopped.')
            engine_on = False
        else:
            print('Car is already stopped!')
    elif command == 'quit':
        print('Bye!')
        break
    else:
        print('Oops! I dont understand this yet!')
        continue
print('Thanks for playing!')
```
- My brain is super huge. Before Mosh tells me to take this program to next level by not repeating car start/stop messages, I have already done that in the exact way. *This is what you call **Critical Thinking** I guess*. 
 
---
### For Loops

- Already mastered? ')

### Range function

- To produce a list of integers until the stop index
- range(n) - -> 0,...,n-1

Example:
```python
print(range(10))
#1,2,3,4,5,6,7,8,9(n-1)

print(range(0,4))
#0,1,2,3
```

- Or we can add 
  - *starting point*
  - *ending point*
  - *step*(difference/progression)

Example:
```python
for i in range(0,20,3) #from 0->20 with +3 increment every time
    print(i)
    #0 3 6 9 12 15 18
```
> A small program using for loops
- A program to find the total cost of the shopping cart listed out.

Solution:
```python
prices = list()
while True:
    #taking input with the key deadword
    price = input('Enter the price(enter /done/ once you are done):')
    if price.rstrip().lower() == 'done':
        break
    else:
        prices.append(int(price))
#cost    
total_cost = 0
for p in prices:
    total_cost += p
print(f"Total Cost is: ${total_cost}.")
```    
---
### Nested Loops
- Printing out coordinates(x,y)
```python
for x in range(4):
    #for each incrementation of x, 4 values of y come along
    for y in range(4):
        print(f"({x},{y})")
#Output
# (0,0)
# (0,1)
# (0,2)
# (0,3)
# (1,0)
# (1,1)
# (1,2)
# (1,3)
# (2,0)
# (2,1)
# (2,2)
# (2,3)
# (3,0)
# (3,1)
# (3,2)
# (3,3)

#lets do xyz
for x in range(4):
    for y in range(4):
        for z in range(4):
            print(f"({x},{y},{z})")
#output
#(0,0,0)
#(0,0,1)
# .
# .
# .
# (3,3,3)
```
> Another tough challenge using range()
- We have to print out this
```
xxxxx
xx
xxxxx
xx
xx
```
- Wow, that was fairly easy. 
Code:
```python
numbers = [5,2,5,2,2]
for i in numbers:
    print('x'*i)
#this is not the way :')
```
- Next attempt(not easy at all)
Code:
```python
numbers = [5,2,5,2,2]
for i in numbers:
    output = ''
    for k in range(i):
        output += 'x'
    print(output)

#L shape
numbers = [1,1,1,1,4]
for i in numbers:
    output = ''
    for k in range(i):
        output += 'x'
    print(output)
```
---
### Lists
- A bit mastered :)
> A list exercise :')
- Find the largest number in the list
Code:
```python
numbers = list()
while True:
    try:
        number = input('Enter a number(/done/ when you are done:')
        numbers.append(int(number))
    except:
        if number.lower() == 'done':
            break
        else:
            print('Please only enter numbers!:')
            break
if numbers == []:
    print('Your list is empty. You entered only unaccessible inputs!\n\nOr you did not enter a single input.')
else:
    print(f"Your list of numbers: {numbers}")
    largest_int = None
    for i in numbers:
        if largest_int == None:
            largest_int = i
        elif largest_int < i:
            largest_int = i
    print(f"Largest number is {largest_int}.")
```
--- 
### 2D Lists

- Like a matrix in math
```
[
    1 2 3
    4 5 6
    7 8 9
]
```
- Defining that matrix with list:
```python
matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]
#Accessing values will be like matrix[0][0] --> matrix[2][2]
```
---
### List methods

- I know a bit.

```python
.insert()   #insert at certain index
.append()   #added to the end of the list
.remove()   #remove the element at that index(only remove the first occurance)
.clear()    #empties the list
.pop()      #remove the last list item
.index()    #search for certain numbers index
.count()    #count the occurances of a certain character
.sort()     #sort the list(doesn't return anything)
.reverse()  #reverse sort the list
.copy()     #copy the list into another list
```

> Write a program to remove duplicates in a list.
- I was right. It just needs to remove the duplicates and leave one only.
Code:
```python
numbers_list = list()
#input checking and receiving
while True:
    try:
        number = input('Enter a number(/done/ when you are done:')
        numbers_list.append(int(number))
    except:
        if number.lower() == 'done':
            break
        else:
            print('Please only enter numbers!:')
            break
#empty list
if len(numbers_list) == 0:
    print('Your list is empty.\nYou may have entered no input (or) only unaccessible inputs.')
else:
    print('Your original list:', numbers_list)
    #removing duplicates
    for i in numbers_list:
        if numbers_list.count(i) > 1:
            numbers_list.remove(i)
        else:
            continue
    print('Your list with no duplicates:', numbers_list)
#no this was easy I was just overcomplicating things
```
- That was funny XD

---
### Tuples

- Immutable lists(*that's about it)
- Uses () instead of [].
- If we want a memory efficient and no-need-to-modify list, tuple is for you. 
- Only two functions available 
  - .count()
  - .index()
---
## Unpacking

- Putting all values inside a tuple(only?) into separate variables.
```python
coordinates = (1,2,3) #tuple

x,y,z = coordinates #three elements inside the tuple are now each assigned into x, y and z respectively.(x=1,y=2,z=3)
```
- Quite cool tbh.
*has to get the exact number of variables as the number of the tuple's elements I guess.*

__*We can use this with lists as well!*__ .

```python
coordinates = [1,2,3]
x,y,z = coordinates
```
---
### Dictionaries

- Like objects in JS
- Key-value pairs
- Super handy stuff

Code
```python
customer = {
    "name":"Ken",
    "age": 19,
    "is_verified":True,
    69: "No"
}
```
- Each key should be unique.(no duplicate keys allowed)

Accessing them(case sensitive):
```python
customer["is_verified"] #True
```

- **.get()** method
```python
customer.get("birthdate","Jan 17")
```
> A program to convert 1234 into its english words.(any order)

Code
```python
numb_to_word = {
    1:'One',
    2:'Two',
    3:'Three',
    4:'Four',
    5:'Five'
}
number = input("Enter:")
#to get the output as a string
output = ""
for n in number:
    output += numb_to_word.get(int(n), '!')+ " " 
    #added that number and ' ' to output
print(output)

```
---
### Emoji Converter :)(with Dict)

- Converter from text emoji to emoji
- Dict will map text emojis to the actual emojis.
Code:
```python
#Emoji Converter to convert any text form emoji into real emojis

message = input(">")
words = message.split()

#pairing the emojis (only a handful for now)
emojis = {
    ":)": "🙂",
    ":(": "🙁",
    ":')":"😅",
    ":'(":"😢",
    ":3":"😖",
    "xD":"😆"
}
output = ""
#not really impressive as I thought tho 
for word in words:
    output += emojis.get(word, word) + " " 
print('\n',output)
```
---
### Functions

- Everyone's favorite thingy :)
- If we want to (or) have to use a chunk of code more than once then we can use functions to call them and use it all the way.

Example:
```python
def add(a,b):
    print(a+b)
def add(a,b):
    return a+b
```
Recalling the function:
```python
print('Sum', add(c,d))
```

- We can provide *keyword arguments* to functions which will fill up the function's parameters.

Example:
```python
def greet(first_name,last_name);:
    print(f'Hey {first_name} {last_name}!')

print("Start")
greet(first_name="Ken",last_name="V") #any order is fine
print("finish")
```
- When using keyword arguments, we have to put them **after** positional arguments.(pythonista ways 3)
- When most of the time, use positional arguments but when dealing with multiple commplex numerical arguments.

---
### Return Statement

- Already mastered
- We have to store the result in a variable tho.
- When there is no return statement in a function and we call it back, it will just grab a **None**.

---
### Reusable function

Putting the emoji converter into a reusable function. *(will just copy it)*

> Code:
```python
message = input('>')
def text_emoji(text):
    words = text.split()
    emojis = {
        ":)": "🙂",
        ":(": "🙁",
        ":')":"😅",
        ":'(":"😢",
        ":3":"😖",
        "xD":"😆"
    }
    output = ""
    #not really impressive as I thought tho 
    for word in words:
        output += emojis.get(word, word) + " " 
    return output
print("Output:", text_emoji(message))
```
---
### Exception Handling(error handling)

- Already mastered
We use this when we want the program to display something at least when the user enters an invalid input instead of showing *traceback* and quit. 

Example Syntax:
```
try:
    do something unless
except:
    this error occurs
```
Code:(*when user enters an invalid numerical input)
```python
try:
    age = int(input('Age>'))
    print(age)
except ValueError:
    print("Invalid Value! Try again!")

```
#### Cool my notes about objects classes and inheritances are now long gone.

### Classes and Objects

- Classes are the types we create(like list,dicitionaries) and use for our specific purposes.
- Objects are instances of classes to be used more than once.

> Example: We want to define a custom class that represents mammals and we want to use it for dogs and cats.
```python
#defining a parent class
class Mammal:
    def walk(self):
        print("I'm walking...")
        
#inheritant classes(dog and cat)
#we have to put in the name of the parent class just after the class's name

class dog(Mammal):
    #we can add specific methods for specific classes as well
    def bark(self):
        print('Woof Woof Woof')
class cat(Mammal):
    def meow(self):
        print('Meow meow meow')

#We cannot have empty classes in python so we just add a 'pass' to let it pass.

#dog and cat will have now same properties,methods as Mammal.
dog1 = dog()
dog1.walk()
dog1.bark()
cat1 = cat()
cat1.walk()
cat1.meow()
```
---
### Modules

- When we want to refer to a specific python file in multiple files, we call that a *module*.
- We can make a python module(**a regular file**) and, recall it(**import**) in whichever programs we want to use them in.
- We use modules so our main python program is not bombarded with functions we might want to reuse a bunch of times in other programs as well.
- *Modules are just a bunch of python files where they refer to each other or vice versa*. 

Importing the module file:
```python
import file_name
```
Importing the specific function of the module:
```python
from file_name import function_name
```
- this doesn't work in my machine tho. Looks like I forgot to add the python path again. But I know how to do it so hey.
- **It finally fucking works!!! with path intellisense.**.
---
### Packages

Pip?
- package is a container for multiple modules(each with its own purpose).

Creating a package: 
- make a new folder(directory)
- add a file named `__init__.py` inside the directory.(*now this will be a python package*)
- then add modules.
  
Importing a package:
- the same as importing a module.
```python
import package_name
```
Importing a module inside of a package:
```python
import package_name.module_name
```
everytime we use a function from that package.
or 
```python
from package_name import module_name
```
*Packages are quite important especially when working frameworks like django.*

---
### Generating Random Values

- Not really random innit ').

Usage:
> random.random()
```python
import random
for i in range(4):
    print(random.random())
#four random values
```
> random.randint(start,finish) *including min,max*
```python
import random
for i in range(4):
    print(random.randint(20,30)) #random between 20 and 30 only
```

> random.choice(list) *random from a list*
```python
import random 
candidates = ['John','Vex','Jason','Juan']
print(random.choice(candidates))
```

> Exercise: Write a program that will generate random dice results. Instructions: define a 'Dice' class that has roll() method that will return a tuple after each roll.

Solution:
```python
import random
numbers = (1,2,3,4,5,6)
class Dice:
    def roll(self):
        return random.choice(numbers),random.choice(numbers) #had to search for this 
dice1 = Dice()
print(dice1.roll())
```
---
### Files and Directories

Pathlib - module used for Object-oriented filesystem paths

Importing module:
```python
from pathlib import Path
```
To use Path(class), we have to define objects:
- Two Paths
  - absolute paths(*starts from root of our hardisk*)
  - relative paths(*starts from current directory*)

Example:
```python
from pathlib import Path # (class)

# have to create an path object
path = Path("crash") #between the () is path_name
#checking whether it exists or not
print(path.exists())
#same linux commands in creating and deleting dirs/files

#if path does not exist, we can make it by 
# path.mkdir()
#deleting the directory/file
path.rmdir()
```

Accessing all files in a path(dir):
```python
path = Path()
print(path.glob('*'))
```
- we have to enter a search pattern as an argument in the glob (pattern the same as git)

Example: search for all python files
```python
print(path.glob('*.py'))
```
- returns `<generator object Path.glob at 0x000002CC9D843890>`
  - we can loop through them when automating tasks and shit
- For looping through it:
```python
for file in path.glob('*'):
    print(file)
```
This will print all the files in the current directory running in **Terminal**.(if I opened a folder in VScode and run this, it will just open files in that particular folder).

---
### Pypi and Pip(Huh? 3)

>Pypi - *python package index*
- we can find thousands of packages here(already published by people)
- for example, if we want to write a program sending sms, we can just find and grab a package related.(*not entirely bug-free tho*)

#### Installing Pypi packages
- pip install package_name into terminal(that's it) in our current working folder?
- I think it will just install it in current directory.
- And we can import the package and its modules. dada
---
>**Mosh is saying we are done with basic python concepts lol xD. Okay the rest, I think, is just a little bit of everything.(django,flask?,automation,ai?). Will complete this and then move on to the course and mit's python.**


----
# This is the end of mosh's Python course. The rest are the projects :)

# Mosh's Python Complete Course Notes(Course+ lol)

*The audio quality here is a complete mess but I guess that's what you get for free.* 
## Data Structures

<!--TODO: watch this after reading about lambdas  -->
## Lambdas Functions/Expressions

## Map Function

## Filter Function
FIXME:

# Zip Function

*Example:* Say we want to combine two lists into a list with each list item being a tuple of the elements in two lists with the same index.
```python
list1 = [1,2,3]
list2 = [10,20,30]
#Result wanted: [(1,10),(2,20),(3,30)]
for i in zip(list1,list2): #result 
    print(i)
#or we can convert it to list by using 'list'
print(list(zip(list1,list2)))
```
*pretty cool*
- This zip function will zip anything we pass in even a string with two lists or something(same length).
- If we give something with the different length, it will expand into minimum length possible. Example:
```python
print(list(zip('123',list1,list2,'20')))
#[('1', 1, 10, '2'), ('2', 2, 20, '0')] /the '3' at the first element is ignored
```
---
## Stacks

*Very important*

- resembles stacks of items.
- LIFO(last in first out)
- the last one added will be the one removed first.
Example: Like a stack of books, the last book you put on the stack is the first/easiest one to be removed as well.

>code:
```python
#stack is basically just a list which follows certain rules and principles of a stack
browsing_session = []
browsing_session.append(1)
browsing_session.append(2)
browsing_session.append(3)
#stack is formed
print(browsing_session)
#LIFO so we can remove the last one in with pop()
last = browsing_session.pop() #returns the popped value(last one)
print("Popped:", last)
print(browsing_session)
#now the last_one is '2' which is [-1] as always will be
print("Back to",browsing_session[-1]) #always the last one in
#checking if the stack is empty or not
if not browsing_session:
    print("Disable! No more rollbacks.") #if we loop through the stack it will eventually reach to this
#and then we loop through this stack with the same principle as this.
```
- Example Usage: browsing sessions, data updates?
---
## Queues

*Very important as well.*

- **FIFO**(*first in first out*)
- Like a queue(*of people*) in real world, first person to get in the queue will be the first one to get out.
- Also just a list with queue principles.

>Example:
```python
#we have to import a class from a module
from collections import deque
#wrapping the empty list with the deque object
#this has some extra properties/methods that can be used in objects like ".appendleft" ".popleft"
queue = deque([])
queue.append(1)
queue.append(2)
queue.append(3)
queue.popleft() #first one will be removed(FIFO)
print(queue) #OUTPUT--| deque([2,3])

#checking for emptiness
if not queue:
    print("empty")
#if we loop through the queue, we will soon likely to encounter empty queue so we can do that.
```

### Swapping variables

We normally needs a third variable(empty socket) when we want to swap values between two variables. But python says no need to sweat lol. 
>Code:
```python
x,y = 12,90
print(f"X: {x} , Y: {y}")

x,y = y,x
print("Swapped")
print(f"X: {x} , Y: {y}")
```
---
## Arrays 

*Super important and not sweer ')*








