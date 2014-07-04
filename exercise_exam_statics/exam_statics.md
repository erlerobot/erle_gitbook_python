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
- The next step in the creation of our grade statistics program involves computing the mean (average) of the grades.
 + Define a function `grades_sum()` that does the following.
 + Takes in a list of scores, scores
 + Computes the sum of the scores
 + Returns the computed sum
 + Call the newly created `grades_sum()` function with the list of grades and print the result.

**Solution 2**
```
>>> grades = [100, 100, 90, 40, 80, 100, 85, 70, 90, 65, 90, 85, 50.5]
>>>
>>>
>>>
>>> def grades_sum (scores):
...     total = sum (scores)
...     return total
...
>>>
>>> print grades_sum(grades)
1045.5
>>>
>>>
```
- Define a function `grades_average()`, below the grades_sum() function that does the following:

 + Has one argument, grades, a list
 + Calls `grades_sum` with grades
 + Computes the average of the grades by dividing that sum by float(len(grades)).
 + Returns the average.
 + Call the newly created `grades_average()` function with the list of grades and print the result.

**Solution 3**
```
>>> def grades_average(grades):
...     tot =grades_sum(grades)
...     ave=tot/float(len(grades))
...     return ave
...
>>> print grades_average(grades)
1045.5
```

