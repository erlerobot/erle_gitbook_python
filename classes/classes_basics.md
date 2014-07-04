## Classes basics

A class is basically a scope inside which various code (especially function definitions) is executed, and the locals to this scope become attributes of the class, and of any objects constructed by this class.

Python is an object-oriented programming language, which means it manipulates programming constructs called objects. You can think of an object as a single data structure that contains data as well as functions; functions of objects are called methods. For example, any time you call `len("Eric")`
Python is checking to see whether the string object you passed it has a length, and if it does, it returns the value associated with that attribute. When you call `my_dict.items().
Python checks to see if my_dict has an items() method (which all dictionaries have) and executes that method if it finds it.

But what makes "Eric" a string and my_dict a dictionary? The fact that they're instances of the str and dict classes, respectively. In other words,a class is just a way of organizing and producing objects with similar attributes and methods.

#####Class syntaxis

A basic class consists only of the class keyword, the name of the class, and the class from which the new class inherits in parentheses. For now, our classes will inherit from the object class, like so:
```
class NewClass(object):
```
This gives them the powers and abilities of a Python object. By convention, user-defined Python class names start with a capital letter.

######Practice 1
Create a class called `Animal in the editor. For now, in the body of your class, use the `pass` keyword. (`pass` doesn't do anything, but it's useful as a placeholder in areas of your code where Python expects an expression.)
Don't loose this code, we are going to continue modifying it in next practices of this section.
```
>>> class Animal(object):
...       pass
...
>>>
```
---

We'd like our classes to do more than... well, nothing, so we'll have to replace our `pass` with something else.

##### Initializing classes
We  should start our class definition off with an odd-looking function: `__init__()`. This function is required for classes, and it's used to initialize the objects it creates. `__init__()` always takes at least one argument, `self`, that refers to the object being created. You can think of `__init__()` as the function that "boots up" each object the class creates.

######Practice 2
Remove the pass statement in your class definition, then go ahead and define an `__init__() `function for your `Animal` class. Pass it the argument `self` for now. Finally, put the pass into the body of the `__init__() definition, since it will expect an indented block.
```
>>> class Animal(object):
...     def  __init__(self):
...         pass
...
...
>>>
```
---
Let's make one more tweak to our class definition, then go ahead and instantiate (create) our first object.

So far, `__init__()` only takes one parameter: `self`. This is a Python convention; there's nothing magic about the word "self". However, it's overwhelmingly common to use self as the first parameter in `__init__()`, so you should do this so that other people will understand your code.

The part that is magic is the fact that self is the first parameter passed to `__init__()`. Python will use the first parameter that `__init__()` receives to refer to the object being created; this is why it's often called self, since this parameter gives the object being created its identity.

######Parctice 3
Pass `__init__()` a second parameter, name.
In the body of `__init__()`, let the function know that name refers to the created object's name by typing `self.name = name`.

```
>>> class Animal(object):
...     def  __init__(self, name):
...         self.name=name
...
...
>>>

```
---
#####Access attributes of objects
We can access attributes of our objects using dot notation.

Here's how it works:
```
>>> class Square(object):
...   def __init__(self):
...     self.sides = 4
...
>>> my_shape = Square()
>>> print my_shape.sides
4
>>>
```
######Practice 4
Outside the `Animal` class definition, create a variable named `zebra` and set it equal to `Animal("Jeffrey")`.
Then print out zebra's name.
```
>>> class Animal(object):
...     def  __init__(self, name):
...         self.name=name
...
...
>>> zebra=Animal("Jeffrey")
>>> print zebra.name
Jeffrey
```
---

As mentioned, you can think of `__init__()` as the method that "boots up" a class' instance object: the init bit is short for "initialize."

The first argument `__init__()` gets is used to refer to the instance object, and by convention, that argument is called self. If you add additional arguments—for instance, a name and age for your animal—setting each of those equal to `self.name` and `self.age` in the body of `__init__()` will make it so that when you create an instance object of your Animal class, you need to give each instance a name and an age, and those will be associated with the particular instance you create.

######Practice 5
Analyze this code. You can copy it in a file calles ` animals.py` and execute it. What happend?
```
# Class definition
class Animal(object):
    """Makes cute animals."""
    # For initializing our instance objects
    def __init__(self, name, age, is_hungry):
        self.name = name
        self.age = age
        self.is_hungry=is_hungry

# Note that self is only used in the __init__()
# function definition; we don't need to pass it
# to our instance objects.

zebra = Animal("Jeffrey", 2, True)
giraffe = Animal("Bruce", 1, False)
panda = Animal("Chad", 7, True)

print zebra.name, zebra.age, zebra.is_hungry
print giraffe.name, giraffe.age, giraffe.is_hungry
print panda.name, panda.age, panda.is_hungry
```
Execution:
```
root@erlerobot:~/Python_files# python animals.py
Jeffrey 2 True
Bruce 1 False
Chad 7 True
root@erlerobot:~/Python_files#
```
---

#####Class scope

Another important aspect of Python classes is scope. The scope of a variable is the context in which it's visible to the program.

It may surprise you to learn that not all variables are accessible to all parts of a Python program at all times. When dealing with classes, you can have variables that are available everywhere (global variables), variables that are only available to members of a certain class (member variables), and variables that are only available to particular instances of a class (instance variables).

The same goes for functions: some are available everywhere, some are only available to members of a certain class, and still others are only available to particular instance objects.

For example:
```
class Animal(object):
    """Makes cute animals."""
    is_alive = True
    def __init__(self, name, age):
        self.name = name
        self.age = age
```
Each individual animal gets its own name and age (since they're all initialized individually), but they all have access to the member variable `is_alive`, since they're all members of the Animal class.
