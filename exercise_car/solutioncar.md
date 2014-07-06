## Solution:Car
 Store this code in a file called `car.py`. This code bellow to the last question of the exercise:
 ```
 class Car(object):
    condition = "new"
    def __init__(self, model, color, mpg):
        self.model = model
        self.color = color
        self.mpg   = mpg

    def display_car(self):
      return "This is a %s %s with %s MPG." % (self.color,self.model,str(self.mpg))

    def drive_car(self):
        self.condition="used"

class ElectricCar(Car):
    def __init__(self,model, color, mpg, battery_type):
        self.model = model
        self.color = color
        self.mpg   = mpg
        self.battery_type=battery_type

    def drive_car(self):
        self.condition="like new"



my_car=ElectricCar("DeLorean", "silver", 88,"molten salt")
print my_car.condition
my_car.drive_car()
print my_car.condition
```
The execution should result on:

```
root@erlerobot:~/Python_files# python menu.py
new
like new
root@erlerobot:~/Python_files#
```
