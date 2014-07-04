## Member variables and functions

#####Methods

When a class has its own functions, those functions are called methods. You've already seen one such method:` __init__()`. But you can also define your own methods.

######Practice 1
Going back to the `Animals`example, where we have this code:
```
class Animal(object):
    """Makes cute animals."""
    is_alive = True
    def __init__(self, name, age):
        self.name = name
        self.age = age
```
Add a method, `description, to your `Animal` class. Using two separate print statements, it should print out the name and age of the animal it's called on. Then, create an instance of Animal, hippo (with whatever name and age you like), and call its description method.

Answer, copy this in a file called `hippo.py`:
```
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
