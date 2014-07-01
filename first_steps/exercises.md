## Exercises

######Exercise 1


Assume that we execute the following assignment statements:
width = 17
height = 12.0
For each of the following expressions, write the value of the expression and the
type (of the value of the expression).
1. width/2
2. width/2.0
3. height/3
4. 1 + 2 * 5
Use the Python interpreter to check your answers.



######Exercise 2

You've finished eating at a restaurant, and received this bill:
```
Cost of meal: $44.50
Restaurant tax: 6.75%
Tip: 15%
You'll apply the tip to the overall cost of the meal (including tax).
```
Steps to follow:

- First, let's declare the variable meal and assign it the value 44.50.

- Now let's create a variable for the tax percentage:
The tax on your receipt is 6.75%. You'll have to divide 6.75 by 100 in order to get the decimal form of the percentage.
Create the variable tax and set it equal to the decimal value of 6.75%.

- You received good service, so you'd like to leave a 15% tip on top of the cost of the meal, including tax.
Before we compute the tip for your bill, let's set a variable for the tip. Again, we need to get the decimal form of the tip, so we divide 15.0 by 100.
Set the variable tip to decimal value of 15% .


- Reassign in a Single Line
 We've got the three variables we need to perform our calculation, and we know some arithmetic operators that can help us out.
(We saw in 3.3 Variables that we can reassign variables. For example, we could say spam = 7, then later change our minds and say spam = 3.)
Reassign meal to the value of `itself + itself * tax`.

- We're only calculating the cost of meal and tax here. We'll get to the tip soon. Let's introduce on new variable, total, equal to the new `meal + meal * tip`.

- Insert at the end this code `print("%.2f" % total). This code print to the console the value of total with exactly two numbers after the decimal.

######Exercise 3
Practicing with string variables, follow the steps:

1. create the variable `my_string` and set it to any string you'd like.
2. print the length of `my_string`.
3. print `my_string`on capital letters.


######Exercise 4
Write a program to prompt the user for hours and rate per hour to compute gross pay. The data should be:
```
Enter Hours: 35
Enter Rate: 2.75
Pay: 96.25
```

######Exercise 5

Print the date and time together in the form: `mm/dd/yyyy hh:mm:ss`.

######Exercise 6
Write a program which prompts the user for a Celsius temperature,convert the temperature to Fahrenheit and print out the converted temperature.
Note:` ºC *9/5 +32 = ºF



##Solutions

######Exercise 1


```
root@erlerobot:~# python
Python 2.7.3 (default, Sep 26 2013, 21:37:06)
[GCC 4.6.3] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> width = 17
>>> height = 12.0
>>>
>>> width/2
8
>>> width/2.0
8.5
>>> height/3
4.0
>>> 1+ 2*5
11
>>>
```

######Exercise 2
```

>>> meal = 44.50
>>> tax = 6.75/100
>>> tip = 15.0/100
>>> meal = meal + meal * tax
>>> total=meal +meal*tip
>>> print("%.2f" % total)
```

######Exercise 3
````
>>> my_string= 'Erle'
>>> # For printing the length of the string we use len() method.
>>> print len(my_string)
4
>>> # For displaying the string in Capital letters we use upper() method.
>>> print my_string.upper()
ERLE
>>>

````

######Exercise 4
```

>>> hours=raw_input('Enter worked hours:')
Enter worked hours: 35
>>> hours=int(hours)
>>> rate=raw_input('Enter rate of payment:')
Enter rate of payment:2.75
>>> rate=float(rate)
>>> #Notice that we change from string to integer/float before using math operators.
...
>>> pay= hours*rate
>>> print "the pay is:", pay
the pay is: 96.25
>>>
```

######Exercise 5

```
>>> from datetime import datetime
>>> now = datetime.now()
>>>
>>> print '%s/%s/%s %s:%s:%s' % (now.month, now.day, now.year,now.hour, now.minute, now.second)
7/1/2014 19:4:35
>>>
```

######Exercise 6

```
>>> tempC= raw_input('Enter de temperarute in Celsius:')
Enter de temperarute in Celsius:20
>>> tempC=float(tempC)
>>> #We change from string to float, so we can use operators.
...
>>> tempF=tempC*(9/5) +32
>>> print "The temperature in farenheit is:", tempF
The temperature in farenheit is: 52.0
>>>
```
