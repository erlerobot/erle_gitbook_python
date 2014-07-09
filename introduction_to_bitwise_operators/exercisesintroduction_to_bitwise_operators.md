## Exercises:Introduction to Bitwise Operators

######Exercise 1
We have the variable `a = 0b10111011`.
Use a bitmask and the value a in order to achieve a result where the third bit from the right of a is turned on. Be sure to print your answer as a `bin()` string.

######Exercise 2

 We have the variable `a = 0b10111011`..Use a bitmask and the value a in order to achieve a result where all of the bits in a are flipped. Be sure to print your answer as a `bin()` string.

######Exercise 3
Define a function called `flip_bit that takes the inputs (number, n).
Flip the nth bit (with the ones bit being the first bit) and store it in result.
Return the result of calling bin(result).

##Solutions
######Exercise 1
```python
>>> a = 0b10111011
>>>
>>> bitmask = 0b100
>>> print bin(a | bitmask)
0b10111111
```
######Exercise 2
```python
>>> a = 0b11101110
>>> mask = 0b11111111
>>> result = a^mask
>>> print bin(result)
0b10001
>>>

```
######Exercise 3
```python
>>> def flip_bit(number,n):
...     mask=(0b1<<n-1)
...     return bin(number^mask)
...
>>>
>>> flip_bit(0b1000111,4)
'0b1001111'
>>>
```
Note:`mask=(0b1<<n-1)`is going to slide over a number or add zeros to this particular number starting from the right and going left
