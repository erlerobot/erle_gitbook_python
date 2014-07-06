## Member variables and functions

#####Methods

When a class has its own functions, those functions are called methods. You've already seen one such method:` __init__()`. But you can also define your own methods.

######Practice 1
Going back to the `Animals`example, where we have this code:
```python
class Animal(object):
    """Makes cute animals."""
    is_alive = True
    def __init__(self, name, age):
        self.name = name
        self.age = age
```
Add a method, `description, to your `Animal` class. Using two separate print statements, it should print out the name and age of the animal it's called on. Then, create an instance of Animal, hippo (with whatever name and age you like), and call its description method.

Answer: copy this in a file called `hippo.py`:
```python
class Animal(object):
    """Makes cute animals."""
    is_alive = True
    def __init__(self, name, age):
        self.name = name
        self.age = age


    def description(self):
        print self.name
        print self.age

hippo=Animal("George","12")
print hippo.description()
```
Here you have the result of the execution:
```
root@erlerobot:~/Python_files# python hippo.py
George
12
None
root@erlerobot:~/Python_files#

```
---

#####Member variables

A class can have any number of member variables. These are variables that are *available to all members* of a class.

######Practice 2

You have this piece of code:
```python
class Animal(object):
    """Makes cute animals."""
    is_alive = True #This is the member variable
    def __init__(self, name, age):
        self.name = name
        self.age = age


    def description(self):
        print self.name
        print self.age

hippo=Animal("George","12")
print hippo.description()
```

After line 3, add a second member variable called `health` that contains the string "good".
Then, create two new Animals: `sloth` and `ocelot`. (Give them whatever names and ages you like.)
Finally, on three separate lines, print out the health of your hippo, sloth, and ocelot.

Answer:store this code in a file:
```python
class Animal(object):
    """Makes cute animals."""
    is_alive = True #This is the member variable
    health="good"
    def __init__(self, name, age):
        self.name = name
        self.age = age


    def description(self):
        print self.name
        print self.age

hippo=Animal("George","12")
print hippo.description()

sloth=Animal("Mani","7")
ocelot=Animal("Prince","2")
print "sloth health:",sloth.health
print "ocelot health:", ocelot.health
print "hippo health:", hippo.health
```
The result when running it :
```
root@erlerobot:~/Python_files# python zoo.py
George
12
None
sloth health: good
ocelot health: good
hippo health: good
root@erlerobot:~/Python_files#

```

