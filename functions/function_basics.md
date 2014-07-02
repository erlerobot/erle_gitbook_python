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

After `def` we find the function argument, between brackets.The empty parentheses after the name indicate that this function doesn’t take any
arguments. Then after the colon and idented to the rigth we find the sentences to run when we call the function.

