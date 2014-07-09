## Logical operators

#####Comparartors

Let's start with the simplest aspect of control flow: comparators. They are use to compare expressions.

|**Comparator**|**Meaning**|
|---|
| == |Equal to |
|!=|Not equal to |
|<|Less than |
|<=|Less than or equal to |
|>|Greater than |
|>=|Greater than or equal to |

Note that `==` compares whether two things are equal, and `= `assigns a value to a variable.

For example:
```python
>>> 17 < 4
False
>>> 3 >= 1
True
>>> 40*2 == 40 +40
True
>>> 1**2 <= -1
False
>>>
```

#####  Boolean Operators

**and operator**

`and` checks if both the statements are True.
```
True and True is True
True and False is False
False and True is False
False and False is False
```

######Practice 1
Let's practice with `and`. Assign each variable to the appropriate boolean value.

- Set `bool_one` equal to the result of` False and False`.
- Set `bool_two` equal to the result of `-(-(-(-2))) == -2 and 4 >= 16**0.5`.
- Set bool_three equal to the result of `19 % 4 != 300 / 10 / 10 and False`.
- Set bool_four equal to the result of `-(1**2) < 2**0 and 10 % 10 <= 20 - 10 * 2`.
- Set `bool_five` equal to the result of` True and True`.

You can check the results in your interpeter:
```python
bool_one = False

bool_two = False

bool_three = False

bool_four = True

bool_five = True
```
---
** or operator**

`or`checks if at least one of the statements is True.
```
True or True is True
True or False is True
False or True is True
False or False is False
```

######Practice 2
Now do the same, but with the `or`operator:

- Set `bool_one` equal to the result of `2**3 == 108 % 100 or 'Cleese' == 'King Arthur'`.
- Set` bool_two equal `to the result of `True or False`.
- Set `bool_three equal` to the result of` 100**0.5 >= 50 or False`.
- Set `bool_four `equal to the result of `True or True`.
- Set `bool_five equal` to the result of` 1**100 == 100**1 or 3 * 2 * 1 != 3 + 2 + 1`.

The result should be:
```python
bool_one = True

bool_two = True

bool_three = False

bool_four = True

bool_five = False
```
---
**not operator**

`not` gives the opposite of the statemen.
```
Not True is False
Not False is True
```

######Practice 6
Let's get some practice with `not`.

- Set `bool_one` equal to the result of` not True`.
- Set `bool_two` equal to the result of `not 3**4 < 4**3`.
- Set `bool_three` equal to the result of `not 10 % 3 <= 10 % 2`
- Set `bool_four` equal to the result of not `3**2 + 4**2 != 5**2`.
- Set `bool_five` equal to the result of `not not False`.

The solution of this practice is:
```python
bool_one = False

bool_two = True

bool_three = True

bool_four = True

bool_five = False
```
---

#####The order of operators

Boolean operators aren't just evaluated from left to right. Just like with arithmetic operators, there's an order of operations for boolean operators:

`not` is evaluated first;
`and` is evaluated next;
`or` is evaluated last.

Parentheses `()` ensure your expressions are evaluated in the order you want. Anything in parentheses is evaluated as its own unit.

###### Practice 4

Assign True or False as appropriate for bool_one through bool_five.

- Set `bool_one` equal to the result of `False or not True and True`.
- Set `bool_two` equal to the result of `False and not True or True`.
- Set `bool_three` equal to the result of `True and not (False or False)`
- Set `bool_four` equal to the result of not not `True or False and not True`.
- Set `bool_five` equal to the result of `False or not (True and True)`.

The solution is the following one:
```python
bool_one = False

bool_two = True

bool_three = True

bool_four = True

bool_five = False
```




