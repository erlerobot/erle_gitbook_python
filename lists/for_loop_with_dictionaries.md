## For loop with dictionaries

The use of `for` when accessing dictionaries is very similar to using this loop with lists.The command should be something like this example:

```
for key in d:
    print d[key]
```

Note that dictionaries are unordered, meaning that any time you loop through a dictionary, you will go through every key, but you are not guaranteed to get them in any particular order.

######Practice 1

We have the following dictionary:
```

webster = {
	"Aardvark" : "A star of a popular children's cartoon show.",
    "Baa" : "The sound a goat makes.",
    "Carpet": "Goes on the floor.",
    "Dab": "A small amount."
}
```
Use a `for` loop to print all the values:

```
>>> webster = {
...     "Aardvark" : "A star of a popular children's cartoon show.",
...     "Baa" : "The sound a goat makes.",
...     "Carpet": "Goes on the floor.",
...     "Dab": "A small amount."
... }
>>>
>>> for key in webster:
...     print webster[key]
...
A star of a popular children's cartoon show.
Goes on the floor.
A small amount.
The sound a goat makes.
>>>
```
