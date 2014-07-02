## Built-in functions

You already know about some of the built-in functions:
- Strings functions, such as `.upper()`, `.lower()`, `str()`, and `len().
- `type()` and type conversion functions: `int()`,`float()`,`str()`.

Now we are going to learn three new functions: `min`, `max`,`abs `.

The `max` and `min` functions give us the largest and smallest values in a list, respectively:

Example with `max`:

```
>>> def biggest_number(*args):
...     print max(args)
...     return max(args)
...
>>> biggest_number(-10, -5, 5, 10)
10
10
>>>
```
Note: The result of print and return is the same.

Example with `min`and strings:
```
>>> min("Erle")
'E'
```

The àbs`function returns the absolute value of a number, let's see an example:
```
>>> def distance_from_zero(arg):
...     print abs(arg)
...     return abs(arg)
...
>>> distance_from_zero(-10)
10
10
```
