## Exercises:Classes


######Exercise 1
Follow the steps:
- Create a class, Triangle. Its `__init__()` method should take `self`, `angle1`, `angle2`, and `angle3` as arguments. Make sure to set these appropriately in the body of the `__init__() `method.
- Create a variable named number_of_sides and set it equal to 3.
- Create a method named `check_angles`. The sum of a triangle's three angles is It should return True if the sum of self.angle1, self.angle2, and self.angle3 is equal 180, and False otherwise.
- Create a variable named `my_triangle` and set it equal to a new instance of your Triangle class. Pass it three angles that sum to 180 (e.g. 90, 30, 60).
- Print out `my_triangle.number_of_sides` and print out `my_triangle.check_angles()`.

######Exercise 2
Define a class called `Songs`, it will show the lyrics of a song.
Its `__init__()` method should have two arguments:`self`anf `lyrics`.`lyrics`is a list.
Inside your class create a method called `sing_me_a_song`that prints each element of `lyrics`on his own line.
Define a varible:
```python
happy_bday = Song(["May god bless you, ",
                   "Have a sunshine on you,",
                   "Happy Birthday to you !"])
```
Call the `sing_me_song`mehod on this variable.


######Exercise 3
Define a class called `Lunch`.Its `__init__()` method should have two arguments:`self`anf `menu`.Where menu is a string.
Add a method called `menu_price`.It will involve a `if`statement:

-  if  "menu 1" print "Your choice:", menu, "Price 12.00", if "menu 2" print "Your choice:", menu, "Price 13.40", else print "Error in menu".

To check if it works define:
`Paul=Lunch("menu 1")` and call `Paul.menu_price()`.

######Exercise 4
Define a Point3D class that inherits from object
Inside the Point3D class, define an `__init__()` function that accepts self, x, y, and z, and assigns these numbers to the member variables `self.x`,` self.y`,` self.z`.
Define a `__repr__()` method that returns `"(%d, %d, %d)" % (self.x, self.y, self.z)`. This tells Python to represent this object in the following format: (x, y, z).
Outside the class definition, create a variable named `my_point` containing a new instance of Point3D with x=1, y=2, and z=3.
Finally, print `my_point`.

##Solutions

######Exercise 1
```python
>>> class Triangle(object):
...     def __init__(self,angle1,angle2,angle3):
...         self.angle1=angle1
...         self.angle2=angle2
...         self.angle3=angle3
...
...     number_of_sides=3
...     def check_angles(self):
...         if self.angle1+self.angle2+self.angle3 ==180:
...             return True
...         else:
...             return False
...
>>> class Equilateral(Triangle):
...   angle = 60
...   def __init__(self):
...        self.angle1 = self.angle2 = self.angle3 = self.angle
...
>>> my_triangle=Triangle(90,30,60)
>>>
>>> print my_triangle.number_of_sides
3
>>> print my_triangle.check_angles()
True
>>>

>>>

```
######Exercise 2
```python
>>> class Song(object):
...   def __init__(self, lyrics):
...      self.lyrics=lyrics
...   def sing_me_a_song(self):
...      for line in self.lyrics:
...           print line
...
>>>
>>> happy_bday = Song(["May god bless you, ",
...                    "Have a sunshine on you,",
...                    "Happy Birthday to you !"])
>>>
>>> print happy_bday.sing_me_a_song()
May god bless you,
Have a sunshine on you,
Happy Birthday to you !
None
>>>
```


######Exercise 3

You can copy this code in a file called `menu.py`:
```python
class Lunch(object):
    def __init__(self,menu):
      self.menu=menu

    def menu_price(self):
       if self.menu=="menu 1":
          print "Your choice:", menu, "Price 12.00"
       elif self.menu=="menu 2":
          print "Your choice:", menu, "Price 13.40"
       else:
          print "Error in menu"

Paul=Lunch("menu 1")
Paul.menu_price()
```
The execution should be:

```
root@erlerobot:~/Python_files# python menu.py
Your choice: menu 1 Price 12.00
root@erlerobot:~/Python_files#
```
######Exercise 4

Copy the following code in a file called `3d.py`:
```python
class Point3D(object):
    def __init__(self,x,y,z):
        self.x=x
        self.y=y
        self.z=z

    def __repr__(self) :
       return "(%d, %d, %d)" % (self.x, self.y, self.z)



my_point=Point3D(1,2,3)
print my_point
```
Now, run the file:
```
root@erlerobot:~/Python_files# python menu.py
(1, 2, 3)
root@erlerobot:~/Python_files#
```
