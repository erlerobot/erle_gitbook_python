## Conditional statements

`if ` is a conditional statement that executes some specified code after checking if its expression is True.

For example:
```
>>> x=10
>>> if x>2 :
...     print "It is a Large number."
...
It is a Large number.
```
Note, the identation is very important here.

The `else` statement complements the `if` statement. An if/else pair says: "If this expression is true, run this indented code block; otherwise, run this code after the else statement."

Unlike `if`, `else doesn't depend on an expression.

Let's see an example:
```
>>> if 8 > 9:
...     print "I don't printed!"
... else:
...     print "I get printed!"
...
I get printed!
>>>
```

`elif` is short for "else if." It means exactly what it sounds like: "otherwise, if the following expression is true, do this!"

Here you find the example:
```
```>>> if 8 > 9:
...     print "I don't get printed!"
... elif 8 < 9:
...     print "I get printed!"
... else:
...     print "I also don't get printed!"
...
I get printed!
```


