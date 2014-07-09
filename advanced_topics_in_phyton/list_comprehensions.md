## List Comprehensions

Let's say you wanted to build a list of the numbers from 0 to 50 (inclusive). We could do this pretty easily:
```python
my_list = range(51)
```
But what if we wanted to generate a list according to some logic—for example, a list of all the even numbers from 0 to 50?

Python's answer to this is the list comprehension. List comprehensions are a powerful way to generate lists using the `for/in` and if keywords we've learned.

For example the list of even numbers, is simply to obtain using:
```python
>>> evens_to_50 = [i for i in range(51) if i % 2 == 0]
>>> print evens_to_50
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50]
>>>
```

######Practice 1

Use a list comprehension to build a list called `even_squares` .
Your `even_squares` list should include the squares of the even numbers between 1 to 11. Your list should start [4, 16, 36...] and go from there.
Remember: When using `range()`you should stop in last_number +1.
```python
>>> even_squares = [i**2 for i in range(1,12) if i % 2 == 0 ]
>>>
>>> print even_squares
[4, 16, 36, 64, 100]
>>>
```
