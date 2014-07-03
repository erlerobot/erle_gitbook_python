
## Identation


#####Whitespace

In Python, whitespace is used to structure code. Whitespace is important, so you have to be careful with how you use it.

######Practice 1
The code on the right is badly formatted.


```
def spam():
eggs = 12
return eggs

print spam()
```
You should see an error message like this one:

```
 File "<stdin>", line 2
    eggs = 12
       ^
IndentationError: expected an indented block
```


Now let's examine.
You'll get this error whenever your whitespace is off.

To correct this you should properly indent the code with four spaces before eggs on line 2 and another four before return on line 3.

You should indent your code with four spaces.
```
>>> def spam():
...     eggs = 12
...     return eggs
...
>>> print spam()
12
```


