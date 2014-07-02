## Function basics

In the context of programming, a function is a named sequence of statements that
performs a computation. When you define a function, you specify the name and
the sequence of statements. Later, you can “call” the function by name.


`def` is a keyword that indicates that this is a function definition. For example:
```
>>> def tax(bill):
...     """Adds 8% tax to a restaurant bill."""
...     bill *= 1.08
...     print "With tax: %f" % bill
...     return bill
...
>>> meal_cost = 100
>>> meal_with_tax = tax(meal_cost)
With tax: 108.000000
>>>
```

Note: `*=`means add that percentage. `tip *=1.6` is the same as adding tip value a 60% : `tip +tip +0.6`.

The function components are:
- The header, which includes the def keyword, the name of the function, and any parameters the function requires.

- An optional comment that explains what the function does.

- The body, which describes the procedures the function carries out. The body is indented, just like for conditional statements.

If you look the example above, after `def` we find the function argument, between brackets.The empty parentheses after the name indicate that this function doesn’t take any
arguments. Then after the colon and idented to the rigth we find the sentences to run when we call the function.

After defining a function, it must be called to be implemented.

######Practice 1

Define a function that returns the square of a number, and call it with the argument 10.
```
>>> def square(n):
...     """Returns the square of a number."""
...     squared = n**2
...     print "%d squared is %d." % (n, squared)
...     return squared
...
... # Call the square function on line 9! Make sure to
... # include the number 10 between the parentheses.
...
>>> square(10)
10 squared is 100.
100
```
######Practice 2

Make the same and kind of function as in Practice 1, but using two arguments:base, exponent.
```
>>> def power(base, exponent):  # Add your parameters here!
...     result = base**exponent
...     print "%d to the power of %d is %d." % (base, exponent, result)
...
>>> power(37,4)  # Add your arguments here!
37 to the power of 4 is 1874161.
```


 A function can call another function, for example:

 ######Practice 3

Define `one_good_turn` (which adds 1 to the number it takes in as an argument) and `deserves_another` (which adds 2).

Change the body of `deserves_another` so that it always adds 2 to the output of `one_good_turn`.
 ```
 >>> def one_good_turn(n):
...     return n + 1
...
>>> def deserves_another(n):
...     return one_good_turn(n) + 2
...
>>> deserves_another(7)
10
>>>
```


