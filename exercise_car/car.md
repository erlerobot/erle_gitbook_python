## Car

We are going to follow the exercise instructions step by step and give solutions to each step, so you canfollow it easily.Also, we will review the conceps shown in classes to fix them.

####Ready? The computing starts here:

- Defining a class is much like defining a function, but we use the **class** keyword instead. We also use the word object in parentheses because we want our classes to inherit the object class. This means that our class has all the properties of an object, which is the simplest, most basic class.

 + Define a new class named "Car". For now, since we have to put something inside the class, use the pass keyword.

 + We can use classes to create new objects, which we say are **instances** of those classes.

 + Below your Car class, create a new object named `my_car` that is an instance of Car.

**Solution 1**
```python
>>> class Car(object):
...     pass
...
... my_car=Car()
>>>
```
- Classes can have member variables that store information about each class object. We call them **member variables** since they are information that belongs to the class object.

 + Inside your Car class, replace the pass statement with a new member variable named `condition and give it an initial value of the string "new".
 + At the end of your code,  use a print statement to display the condition of `my_car`.


**Solution2**
```python
>>>
>>> class Car(object):
...     condition="new"
...
>>> my_car=Car()
>>> print my_car.condition
new
>>>
```

- There is a special function named `__init__() that gets called whenever we create a new instance of a class.The first argument passed to `__init__(`) must always be the keyword `self - this is how the object keeps track of itself internally - but we can pass additional variables after that.In order to assign a variable to the class (creating a member variable), we use **dot notation**.

 + Define the `__init__()` function of the Car class to take four inputs: self, model, color, and mpg. Assign the last three inputs to member variables of the same name by using the self keyword.

 + Then, modify the object my_car to provide the following inputs at initialization:
```
model = "DeLorean"
color = "silver"
mpg = 88
```

**Solution 3**

```python
>>> class Car(object):
...     condition="new"
...     def __init__(self,model,color,mpg):
...      self.model=model
...      self.color=color
...      self.mpg=mpg
...
>>>
>>>
>>>
>>> my_car=Car("DeLorean","silver",88)
>>> print my_car.condition
new
>>>
```
- Calling class member variables works the same whether those values are created within the class (like our car's condition) or values are passed into the new object at initialization. We use dot notation to access the member variables of classes since those variables belong to the object.

 + Now that you've created my_car print its member variables:First print the model of `my_car`.
Then print out the color of `my_car`.Finally, print out the mpg of `my_car.


**Solution 4**
```python
>>> class Car(object):
...     condition="new"
...     def __init__(self,model,color,mpg):
...      self.model=model
...      self.color=color
...      self.mpg=mpg
...
>>> my_car=Car("DeLorean","silver",88)
>>> print my_car.model
DeLorean
>>> print my_car.color
silver
>>> print my_car.mpg
88
>>>
```

- Besides member variables, classes can also have their own **methods** (functions inside the class).

  + Inside the Car class, add a method named `display_car()` to Car that will reference the Car's member variables to return the string, "This is a [color] [model] with [mpg] MPG." You can use the `str()` function to turn your mpg into a string when creating the display string.
 + Replace the individual print statements with a single print command that displays the result of calling `my_car.display_car()`.

**Solution 5**
```python
>>> class Car(object):
...     condition = "new"
...     def __init__(self, model, color, mpg):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...
...     def display_car(self):
...       return "This is a %s %s with %s MPG." % (self.color,self.model,str(self.mpg))
...
>>>
>>> my_car = Car("DeLorean", "silver", 88)
>>> print my_car.display_car()
This is a silver DeLorean with 88 MPG.
>>>

```

- We can modify variables that belong to a class the same way that we initialize those member variables.

 + Inside the Car class, add a method `drive_car() `that sets self.condition to the string "used".
 + Remove the call to `my_car.display_car()` and instead print only the condition of your car.
 + Then drive your car by calling the `drive_car()` method.
 + Finally, print the condition of your car again to see how its value changes.

**Solution 6**
```python
>>> class Car(object):
...     condition = "new"
...     def __init__(self, model, color, mpg):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...
...     def display_car(self):
...       return "This is a %s %s with %s MPG." % (self.color,self.model,str(self.mpg))
...
...     def drive_car(self):
...         self.condition="used"
...
>>>
>>>
>>> my_car = Car("DeLorean", "silver", 88)
>>> print my_car.condition
new
>>> my_car.drive_car()
>>> print my_car.condition
used
>>>
>>>
```
- One of the benefits of classes is that we can create more complicated classes that inherit variables or methods from their **parent classes**. This saves us time and helps us build more complicated objects, since these **child classes** can also include additional variables or methods.
  + Create a class ElectricCar that inherits from Car. Give your new class an `__init__()` method of that includes a "battery_type" member variable in addition to the model, color and mpg.
 + Then, create an electric car named "my_car" with a "molten salt" `battery_type.` Supply values of your choice for the other three inputs (model, color and mpg).

**Solution 7**
```python
>>> class Car(object):
...     condition = "new"
...     def __init__(self, model, color, mpg):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...
...     def display_car(self):
...       return "This is a %s %s with %s MPG." % (self.color,self.model,str(self.mpg))
...
...     def drive_car(self):
...         self.condition="used"
...
>>>
>>>
>>> class ElectricCar(Car):
...     def __init__(self,model, color, mpg, battery_type):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...         self.battery_type=battery_type
...
>>>
>>>
>>>
>>>
>>> my_car=ElectricCar("DeLorean", "silver", 88,"molten salt")
>>>
```
- Since our ElectricCar is a more specialized type of Car, we can give the ElectricCar its own drive_car() method that has different functionality than the original Car class's.
 + Inside ElectricCar add a new method drive_car() that changes the car's condition to the string "like new".
 + Then, outside of ElectricCar, print the condition of `my_car`.
 + Next, drive `my_car` by calling the `drive_car()` function.
 + Finally, print the condition of `my_ca`r again

**Solution 8**
```python
>>>
>>> class Car(object):
...     condition = "new"
...     def __init__(self, model, color, mpg):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...
...     def display_car(self):
...       return "This is a %s %s with %s MPG." % (self.color,self.model,str(self.mpg))
...
...     def drive_car(self):
...         self.condition="used"
...
>>>
>>> class ElectricCar(Car):
...     def __init__(self,model, color, mpg, battery_type):
...         self.model = model
...         self.color = color
...         self.mpg   = mpg
...         self.battery_type=battery_type
...
...     def drive_car(self):
...         self.condition="like new"
...
>>>
>>>
>>> my_car=ElectricCar("DeLorean", "silver", 88,"molten salt")
>>> print my_car.condition
new
>>> my_car.drive_car()
>>> print my_car.condition
like new
>>>
```
