## List Slicing

Sometimes we only want part of a Python list. Maybe we only want the first few elements; maybe we only want the last few. Maybe we want every other element!

List slicing allows us to access elements of a list in a concise manner. The syntax looks like this:
```
[start:end:stride]
```

Where `start` describes where the slice starts (inclusive), `end` is where it ends (exclusive), and `stride` describes the space between items in the sliced list. For example, a stride of 2 would select every other item from the original list to place in the sliced list.(Refer to the index).

For example:
```
>>> l = [i ** 2 for i in range(1, 11)]
>>> # Should be [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
...
>>> print l[2:9:2]
[9, 25, 49, 81]
>>>
```

If you don't pass a particular index to the list slice, Python will pick a default.

- The default starting index is 0.
- The default ending index is the end of the list.
- The default stride is 1.

For example:
```
>>> to_five = ['A', 'B', 'C', 'D', 'E']
>>>
>>> print to_five[3:]
['D', 'E']

>>> print to_five[:2]
['A', 'B']

>>> print to_five[::2]
['A', 'C', 'E']

```

######Practice 1
Given:
```
my_list = range(1, 11) # List of numbers 1 - 10
```
Use list slicing to print out every odd element of my_list from start to finish.
Omit the start and end index. You only need to specify a stride.
```
>>> l = [i ** 2 for i in range(1, 11)]
>>> # Should be [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
...
>>> print l[2:9:2]
[9, 25, 49, 81]
>>>
```
---
#####Reversing a List

We have seen that a positive stride progresses through the list from left to right.A negative stride progresses through the list from right to left should be like this:
```
>>> letters = ['A', 'B', 'C', 'D', 'E']
>>> print letters[::-1]
['E', 'D', 'C', 'B', 'A']
>>>
```
A positive stride length traverses the list from left to right, and a negative one traverses the list from right to left.

Further, a stride length of 1 traverses the list "by ones," a stride length of 2 traverses the list "by twos," and so on.

######Practice 2
Create a variable called `backwards` and set it equal to the reversed version of `my_list = range(1, 11)`.
```
>>> my_list = range(1, 11)
>>>
>>> backwards= my_list[::-1]
>>> print backwards
[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
>>>

```





























