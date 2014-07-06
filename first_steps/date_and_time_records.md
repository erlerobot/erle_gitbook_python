## Date and time Records

A lot of times you want to keep track of when something happened. We can do so in Python using datetime.

Here we'll use datetime to print the date and time in a nice format.

We can use a function called `datetime.now()` to retrieve the current date and time.

```python
>>> from datetime import datetime
>>> print datetime.now()
2014-07-01 16:28:34.848183
>>>
```
The first line imports the datetime library so that we can use it.The second line will print out the current date and time.

You can also store part of the date:
```python
>>> from datetime import datetime
>>> now= datetime.now()
>>> print now.year
2014
>>> print now.month
7
>>> print now.day
1
>>>
```

You can also print `now.hour`, `now.minute`, `now.second`.
