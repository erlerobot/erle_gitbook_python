
## Math operators



With Python you can add, subtract, multiply, divide numbers like this:

- addition = 72 + 23
- subtraction = 108 - 204
- multiplication = 108 * 0.5
- division = 108 / 9
- exponentiation = 2 ** 3
- modulo: Our final operator is modulo. Modulo returns the remainder from a division. So, if you type 3 % 2, it will return 1, because 2 goes into 3 evenly once, with 1 left over.

#####Operators Summary

|**Operator**|**Meaning**|
|------------|------------|
|+|addition|
|-|subtraction|
|*|multiplication|
|/|division|
|**|exponentiation|
|%|remainder of a division|


######Practice 1

We are going to do the following operations:
- Create a integer variable num equal to the sum of two numbers.
- Squar num variable.
- Multiply num from a new variables called num1 equal to the division of two numbers.

```
>>> # create num variable
...
>>> num = 23 +90
>>> # Notice that a variable can be squared
...
>>> num ** 2
12769
>>> #Create the new variable num1
...
>>> num1= 56/71
>>> print num1
0
>>> #Notice that the division gives integers
... num1=float(56/71)
>>> print num1
0.0
>>> #Now num1 is a decimal (float variable)
...
>>> num*num1
0.0
>>>
```

######Practice 2
We are going to follow the steps bellow:
- Create two string variables.
- Sum them.

```
>>>
>>> #Create two string variables
...
>>> var1 = 'Hello'
>>> var2=' World'
>>> #Sum string variables
...
>>> var1+var2
'Hello World'
>>>
```



##### Be careful!

-  When you divide or multiply a integer by a float variable the result becomes float as well.

- You can work with integer, string and float variables. But don't mix string variables with float and integer ones:
```
>>> width+'Hello'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

- When more than one operator appears in an expression, the order of evaluation
depends on the rules of precedence. For mathematical operators, Python follows mathematical convention.
You can use brackets `()`to reorder the operations.
