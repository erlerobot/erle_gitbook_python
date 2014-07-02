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
---


What will the following Python program print out?
```
def fred():
     print "Zap"
def jane():
     print "ABC"

jane()
fred()
jane()
```


- [ ]  Zap ABC jane fred jane
- [ ]  Zap ABC Zap
- [ ]  ABC Zap jane
- [x]  ABC Zap ABC
- [ ]  Zap Zap Zap

> If you compile the code, you can see the answer
```
>>> jane()
ABC
>>> fred()
Zap
>>> jane()
ABC
```

---

######Exercise 4

Rewrite your pay computation program (previus chapter) with time-and-a-half for overtime and create a function called `computepay` which takes two parameters (hours and
rate).
```
Enter Hours: 45
Enter Rate: 10
Pay: 475.0
```

######Exercises 5
```
Let's use functions to calculate your trip's costs:
- Define a function called `hotel_cost` with one argument `nights` as input.
The hotel costs $140 per night. So, the function `hotel_cost` should return 140 * nights.



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

