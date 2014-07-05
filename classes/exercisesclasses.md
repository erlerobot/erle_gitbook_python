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
```
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

##Solutions

######Exercise 1
```
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
```
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
```
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

