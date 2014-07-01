## Variables

Creating web apps, games, and search engines all involve storing and working with different types of data. They do so using variables. A variable stores a piece of data, and gives it a specific name.

For example:

>spam=5

>The variable spam now stores the number 5.

There are different types of variables:integer,string, float(decimal), boolean...
There is an interesting command that tells you of which type the variable is:
```
>>>
>>> #The command type() tells you what type a value has.
...
>>> type(17)
<type 'int'>
>>> type(2.4)
<type 'float'>
>>> type('Hello')
<type 'str'>
>>>
```

#####Booleans

A boolean is like a light switch. It can only have two values. Just like a light switch can only be on or off, a boolean can only be True or False.

You can use variables to store booleans like this:

> a = True

> b = False



#####String variables
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


##### Reassigning values to variables

Now you know how to use variables to store values.

Say my_int = 7. You can change the value of a variable by "reassigning" it, like this:
```
my_int = 3
```
######Practice 2

Try it and see: Change the value of my_int from 7 to 3.


```
root@erlerobot:~/Python_files# python
Python 2.7.3 (default, Sep 26 2013, 21:37:06)
[GCC 4.6.3] on linux2
Type "help", "copyright", "credits" or "license" for more information.

>>> # my_int is set to 7 below. What do you think
... # will happen if we reset it to 3 and print the result?
...
>>> my_int = 7
>>>
>>> # Change the value of my_int to 3 on line 8!
...
>>> my_int =3
>>>
>>> # Here's some code that will print my_int to the console:
... # The print keyword will be covered in detail soon!
...
>>> print my_int
3
>>>

```



