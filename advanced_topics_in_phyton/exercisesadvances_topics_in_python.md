## Exercises:Advances topics in Python

######Exercise 1
Use a list comprehension to create a list, `cubes_by_four.
The comprehension should consist of the cubes of the numbers 1 through 10 only if the cube is evenly divisible by four.
Finally, print that list to the console.
Note that in this case, the cubed number should be evenly divisible by 4, not the original number.

######Exercise 2

Create a variable, `backwards_by_tens`, and set it equal to the result of going backwards through `to_one_hundred` by tens. Go ahead and print `backwards_by_tens` to the console.

######Exercise 3

Create a list, `to_21`, that's just the numbers from 1 to 21, inclusive.
Create a second list, `odds`, that contains only the odd numbers in the `to_21` list (1, 3, 5, and so on). Use list slicing for this one instead of a list comprehension.
Finally, create a third list, `middle_third`, that's equal to the middle third of `to_21, from 8 to 14, inclusive.

##Solutions

######Exercise 1
```
>>> cubes_by_four = [i**3 for i in range(1,11) if i**3 % 4 == 0 ]
>>>
>>> print cubes_by_four
[8, 64, 216, 512, 1000]
```
######Exercise 2
```
>>> to_one_hundred = range(101)
>>>
>>> backwards_by_tens=to_one_hundred[::-10]
>>> print backwards_by_tens
[100, 90, 80, 70, 60, 50, 40, 30, 20, 10, 0]
>>>
>>>
```

######Exercise 3
```
>>> to_21=range(1,22)
>>> print to_21
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21]
>>>
>>> odds=to_21[0::2]
>>> print odds
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21]
>>>
>>> middle_third=to_21[7:14:1]
>>> print middle_third
[8, 9, 10, 11, 12, 13, 14]
>>>

```
