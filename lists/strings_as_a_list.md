## Strings as a list


You can slice a string exactly like a list! In fact, you can think of strings as lists of characters: each character is a sequential item in the list, starting from index 0.If your list slice includes the very first or last item in a list (or a string), the index for that item doesn't have to be included.

######Practice 1
See an example of how managing strings as lists:
```
>>> animals = "catdogfrog"
>>>
>>> cat  = animals[:3]
>>> print cat
cat
>>> # The first three characters of animals
...
>>> dog  = animals[3:6]
>>> print dog
dog
>>> # The fourth through sixth characters
...
>>> frog = animals[6:]
>>> print frog
frog
>>> # From the seventh character to the end
...
>>>
```

