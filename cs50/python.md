# Notes from CS50's W2 lecture: Python

>I really needed to refresh the topics;how convenient!

This course will only teach us the essential concepts so pretty short I'd expect.

## Sets
>Similar to lists but unordered and the elements have to be unique(*no duplicates allowed*): Example:
```python
#create an empty set
s = set()

# add elements to set
s.add(1)
s.add(2)
s.add(3)
s.add(4)
print(s)#{1,2,3,4}
#when an element that's already in the set is added twice, it will be ignored.

# remove elements from set
s.remove(2) #{1,3,4}

# sets length
print(len(s))#3
```

### Dictionaries

Example syntax:
```python
info = {"Name":"Ken","Age":"20"}
```

### Modules
>To use funtions of one file in other files

- If the files and the source module file are in the same directory, we can just import the file or the single function and use it.

Importing a single function:
```python
from file_name import function_name
print("The result:",function_name(a,b))
```
Importing a module(multiple functions):
```python
import module_name
print("The result:",module_name.function_name(a,b))
```
A lot of the problem we might encounter can be resolved by making use of the modules that other devs have already written for the community.

---
### OOP 
We use objects when we want to use custom data structures.
- Class is a blue print for the objects to be built upon it.

How to create a class:
```python
# A custom data structure to represent a point
class Point():
    #every object takes in `self` as an argument
    def __init__(self, x, y):
        # adding properties to this object
        self.x = x
        self.y = y
# We have defined a custom class for the point objects; now we can use it to create point objects.
p = Point(1,3)
# p.x = 1,p.y = 3
```
Adding actions(methods) into classes:
```python
# A program to see if the airplane's capacity can fit the amount of passengers
class Flight():
    def __init__(self, capacity):
        self.capacity = capacity
        self.passengers = []

    def add_passenger(self,name):
        if not self.open_seats():
            return False
        self.passengers.append(name)
        return True

    def open_seats(self):
        return capacity - len(self.passengers)


flight = Flight(3)
people = ["Ken","V","B","J"]
for person in people:
    success = flight.add_passenger(person)
    if success:
        print("Added {person} to flight successfully.")
    else:
        print("There is no available seat for this person.")

```
---
## Decorators
>A way of taking a function and modifying that function by adding new features(behaviors).

- Takes a function as input and returns the modified version of that function as output. 
- This is callled functional programming.
- Also called wrapper function.
```python
def announce(f):
    def wrapper():
            print("About to run the function...")
            f()
            print("Done with the function.")
        return wrapper
# this function just add two more messages to the function and return
# adding announce deco function to hello function
@announce
def hello():
    print("Hello, world!")
```
---
## Lambda
```python
people = [
    {"name":"J","age":20},
    {"name":"K","age":22},
    {"name":"Lol","age":23},
    
]
def f(person):
    return person["name"]

people.sort(key=f)
print(people)
```
- Using a `lambda` expression to solve the above problem:
```python
people.sort(key=lambda person: person["name"])
#person = input;person["name"]  = output
```
---
## Try/Except
Try to do this except some error happens.
```python
import sys
x,y = input("X:"),input("Y:")
try:
    result = x / y
# if this error occurs
except ZeroDivisionError:
    print("Error")
    sys.exit(1)
```

## and bye bye to this lecture.