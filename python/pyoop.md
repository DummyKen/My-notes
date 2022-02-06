# Notes from Corey's Python OOP course

## Classes and Instances(Objects)

Creating a class
```python
class Employee:
    pass #for empty classes
```
Creating objects(instances of classes)
```python
employ_1 = Employee()
employ_2 = Employee()
#two instances having the same general methods/attributes but different values
```

Adding values/attributes to instance variables:
```python
employ_1.first = "Ken"
employ_1.last = "V"
employ_1.email = "banyar@gmail.com"
employ_1.pay = 300000

employ_2.first = "Banyar"
employ_2.last = "Naing"
employ_2.email = "boohoo@gmail.com"
employ_2.pay = 700000
```
so instead of manually setting values for all these instances, we can just define an object and set the attributes of them and set them up later.

Example:
```python
class Employee:
        def __int__(self,first,last,pay): #taking in arguments
        #arguments to attributes
            self.first = first
            self.last = last
            self.pay = pay
            self.email = first + '.' + last + '@gmail.com'
#this is the same as the previous ones assigned each manually
#when defining an instance of this class(object), we can leave off self and just put in other arguments

#defining instances of the Employee class
emp_1 = Employee('Banyar','Naing',30000)
emp_2 = Employee('John','Smith',50000)
#the arguments will fill up the ones in the class
```

- The functions inside of our class variables are called **methods**.
Example:
```python
class Employee:
    #necessary function(initialzing the class?)
    def __init__(self,first,last,pay): #taking in arguments
        #arguments to attributes
        self.first = first
        self.last = last
        self.pay = pay
        self.email = first + '.' + last + '@gmail.com'
    def fullname(self):
        return '{}{}'.format(self.first,self.last)

# instance 
emp_1 = Employee('Ken','V',90)
print(emp_1.fullname) #Ken V
```
**It's important to always put in `self` in every method!**

---
## Class variables 
- variables that are shared between all instances of a class.(*not like instance variables, of which attributes are unique for each instance.*). The attribute of a class variable is the same for all instances of `that` object.

getting too complicated lol :) time for a fun one :)