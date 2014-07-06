
## String variables


Another useful data type is the string. A string can contain letters, numbers, and symbols.

For example:

>name = "Ryan"

>age = "19"

>food = "cheese"


There are some characters that cause problems. For example:

> 'There's a snake in my boot!'

This code breaks because Python thinks the apostrophe in 'There's' ends the string. We can use the backslash to fix the problem(for escaping characters), like this:

>'There\'s a snake in my boot!'


Each character in a string is assigned a number. This number is called the index.


The string "PYTHON" has six characters,
numbered 0 to 5, as shown below:


|** P** | **Y** |** T **|** H **| **O** |** N **|
|----|
|0   |1  | 2 |  3 |  4 |  5|

So if you wanted "Y", you could just type
"PYTHON"[1] (always start counting from 0!).

######Pratice 1
Assign the variable fifth_letter equal to the fifth letter of the string "MONTY".
Remember that the fifth letter is not at index 5. Start counting your indices from zero.

```python
>>> fifth_letter = "MONTY"[4]
>>> print fifth_letter
Y
>>>
```
---

#####String methods

Now that we know how to store strings, let's see how we can change them using string methods.

String methods let you perform specific tasks for strings.

We'll focus on four string methods:`len()`,
`lower()`,`upper()`,`str()`.

**len()**
 The output when using this method will be the number of letters in the string.

```python
>>> parrot="Norwegian Blue"
>>> len(parrot)
14
>>> print len(parrot)
14
```

**lower()**
You can use the `lower()` method to get rid of all the capitalization in your strings.

```python
>>> print parrot.lower()
nowegian blue
```

**upper()**
A similar method exists to make a string completely upper case.
```python
>>> parrot = "norwegian blue"
>>> print parrot.upper()
```
**str()**

Now let's look at str(), which is a little less straightforward. The str() method turns non-strings into strings.

```python
>>> pi=3.14
>>> pi_1= str(pi)
>>> type(pi_1)
<type 'str'>
```

Notice that methods that use dot notation only work with strings.On the other hand, len() and str() can work on other data types.

You can work with integer, string and float variables. But don't mix string variables with float and integer ones when making concatenations:
```python
>>> width+'Hello'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
Sometimes you need to combine a string with something that isn't a string. In order to do that, you have to convert the non-string into a string using `str()``.
```python
>>> print "The value of pi is around " + str(3.14)
The value of pi is around 3.14
```

#####String Formatting with %

When you want to print a variable with a string, there is a better method than concatenating strings together.The `% `operator after a string is used to combine a string with variables. The `% `operator will replace a `%s` in the string with the string variable that comes after it.

######Practice 2
We are going to print a message like this:
" ---- is an awesome ----!". Where instead of --- we will introduce two strings:

```python
>>> string_1="Erle"
>>> string_2="drone"
>>> print " %s is an awesome %s!"%(string_1,string_2)
 Erle is an awesome drone!
>>>
```
