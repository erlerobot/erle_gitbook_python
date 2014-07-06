## Exercises: Functions

######Exercise 1
Write a shutting down program:

First, def a function, `shut_down`, that takes one argument `s`.
Then, if the `shut_down` function receives an `s` equal to "yes", it should return "Shutting down"
Alternatively, elif `s` is equal to "no", then the function should return "Shutdown aborted".
Finally, if `shut_dow`n gets anything other than those inputs, the function should return "Sorry".


######Exercise 2

Import the `math` module in whatever way you prefer. Call its `sqrt` function on the number 13689 and print that value to the console.

######Exercise 3

First, def a function called `distance_from_zero`, with one argument (choose any argument name you like).
If the type of the argument is either `int` or `float`, the function should return the absolute value of the function input.
Otherwise, the function should return "Nope".
Check if it works calling the function with -5.6 and "what?".



######Exercise 4

Rewrite your pay computation program (previus chapter) with time-and-a-half for overtime and create a function called `computepay` which takes two parameters (hours and
rate).
```
Enter Hours: 45
Enter Rate: 10
Pay: 475.0
```

######Exercise 5

Let's use functions to calculate your trip's costs:
- Define a function called `hotel_cost` with one argument `nights` as input.
The hotel costs $140 per night. So, the function `hotel_cost` should return 140 * nights.
- Define a function called `plane_ride_cost` that takes a string, `city`, as input.
The function should return a different price depending on the location, similar to the code example above. Below are the valid destinations and their corresponding round-trip prices.
```
"Charlotte": 183
"Tampa": 220
"Pittsburgh": 222
"Los Angeles": 475
```
-Below your existing code, define a function called `rental_car_cost` with an argument called days.
Calculate the cost of renting the car:
Every day you rent the car costs $40.(cost=40*days)
if you rent the car for 7 or more days, you get $50 off your total(cost-=50).
Alternatively (elif), if you rent the car for 3 or more days, you get $20 off your total.
You cannot get both of the above discounts.
Return that cost.
-Then, define a function called `trip_cost` that takes two arguments, `city` and `days`.
Like the example above, have your function return the sum of calling the `rental_car_cost(days)`, `hotel_cost(days)`, and `plane_ride_cost(city)` functions.
- Modify your `trip_cost` function definion. Add a third argument, `spending_money`.
Modify what the `trip_cost` function does. Add the variable `spending_money to the sum that it returns.

######Exercise 6

Follow the stpes:
- First, def a function called `cube` that takes an argument called `number`.
- Make that function return the cube of that number (i.e. that number multiplied by itself and multiplied by itself once again).
- Define a second function called `by_three` that takes an argument called number.
if that number is divisible by 3,` by_three `should call `cube(number)` and return its result. Otherwise, `by_three` should return False.
-Check if it works.



##Solutions

######Exercise 1
```
>>> def shut_down(s):
...     if s=="yes":
...        return "Shutting down"
...     elif s=="no":
...        return "Shutdown aborted"
...     else:
...        return "Sorry"
...
>>> s="no"
>>> shut_down(s)
'Shutdown aborted'
>>>
```

######Exercise 2
```
>>> from math import sqrt
>>> print sqrt(13689)
117.0

```

######Exercise 3

```

>>> def distance_from_zero(num):
...     if type(num)== int or type(num)== float:
...         return abs(num)
...     else:
...         return "Nope"
...
>>> distance_from_zero(-5.6)
5.6
>>> distance_from_zero("what?")
'Nope'
```
######Exercise 4

```
>>> def computepay(hours,rate):
...     if hours < 40:
...        pay=hours*rate
...        print "the pay is:", pay
...     else:
...        pay = 40 * rate + (hours-40)*1.5*rate
...        print "the pay is:", pay
...
>>>
>>> hours=raw_input("Enter worked hours:")
Enter worked hours:45
>>> hours=float(hours)
>>> rate=10
>>> computepay(hours,rate)
the pay is: 475.0
>>>
```
######Exercise 5
Store this in a file. You can use `vi text editor`and open a `.py` file, save and execute it:
```
root@erlerobot:~# vi trpcal.txt
root@erlerobot:~# cp trpcal.txt trpcal.py
root@erlerobot:~# python trpcal.py
```
This is the code:

```
nights=raw_input("Enter nights:")
city=raw_input("Enter city:")
days=raw_input("Enter days of car rental:")
spending_money=raw_input("Enter money:")

def hotel_cost(nights):
    return 140*nights

def plane_ride_cost(city):
    if city=="Charlotte":
        return 183
    elif city=="Tampa":
        return 220
    elif city=="Pittsburgh":
        return 222
    elif city=="Los Angeles":
        return 475


def rental_car_cost(days):
    cost=days*40
    if days >= 7:
        cost -= 50
    elif days>=3:
        cost-=20
    return cost

def trip_cost(city,days,spending_money):
    print rental_car_cost(days)+hotel_cost(days)+plane_ride_cost(city)+spending_money

trip_cost(city,days,spending_money)
```

######Exercise 6

```
>>> def cube(number):
...     return number*number*number
...
>>> def by_three(number):
...    if number %3 ==0:
...       return cube(number)
...    else:
...       return False
...
>>> by_three(9)
729
>>>
```




