## Iterators for dictionaries

**.items()**

The `.items()`function returns an array of tuples with each tuple consisting of a key/value pair from the dictionary. `.items()` function doesn't return key/value in any specific order.The sintaxis is:

```
print dic_name.items()
```
**.values() and .keys()**

The `.keys()` function returns an array of the dictionary's keys, and
the `.values()` function returns an array of the dictionary's values.
Again, these functions will not return the keys or values from the dictionary in any specific order.
The sintaxis is equal to the `-items()`one.

You can think of a tuple as an immutable (that is, unchangeable) list (though this is an oversimplification); tuples are surrounded by `()`s and can contain any data type.

######Practice 1

Create your own Python dictionary, my_dict, with two or three key/value pairs.
Then, print the result of calling the my_dict.items().
```
>>> my_dict={"string":"string of char",
... "bolean":True,
... "integer":3}
>>>
>>> print my_dict.items()
[('integer', 3), ('bolean', True), ('string', 'string of char')]
>>>

```

Now print the result of using `.keys`and `.values()`:
```
>>> print my_dict.keys()
['integer', 'bolean', 'string']
>>> print my_dict.values()
[3, True, 'string of char']
>>>
```
Remember the other way of iterating throug a dictionary usding the `for`loop.
```
>>>
>>> for key in my_dict:
...     print key, my_dict[key]
...
integer 3
bolean True
string string of char
>>>
```




