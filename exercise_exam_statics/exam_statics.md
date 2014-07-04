## Exam statistics

If you have done the *Battleship exercise*, this one will follow the same structure. We will go step by step, giving solutions in case you get stucked. At the end you can look to the solution file `Exam.py`.

####Ready? The computing starts here:

- This are the grades of some students:
```
grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
```
We are going to make a function to print them.
 + Define a function called `print_grades()` with one argument, a list called grades.
 + nside the function, iterate through grades and print each item on its own line.
 + After your function, call `print_grades()` with the grades list as the parameter.

**Solution 1**
````
>>> grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
>>>
>>> def print_grades(grades):
...     for grade in grades:
...         print grade
...
...
>>> print_grades(grades)
100
100
90
40
80
100
85
70
90
65
90
85
50.5
>>>
```
