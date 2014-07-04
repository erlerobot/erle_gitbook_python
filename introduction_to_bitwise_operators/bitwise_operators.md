## Bitwise operators

**left and right shift bitwise operators**

The next two operations we are going to talk about are the left and right shift bitwise operators. These operators work by shifting the bits of a number over by a designated number of slots.

This operation is mathematically equivalent to floor dividing and multiplying by 2 (respectively) for every time you shift, but it's often easier just to think of it as shifting all the 1s and 0s left or right by the specified number of slots.

Note that you can only do bitwise operations on an integer. Trying to do them on strings or floats will result in nonsensical output.

######Practice 1
Shift the variable `shift_right` to the right twice (>> 2) and shift the variable `shift_left` to the left twice (<< 2). Try to guess what the printed output will be.
```
>>> shift_right = 0b1100
>>> shift_left = 0b1
>>>
>>> shift_right=shift_right >>2
>>> shift_left=shift_left <<2
>>>
>>>
>>> print bin(shift_right)
0b11
>>> print bin(shift_left)
0b100
>>>
```
---
**AND (&) operator**

The bitwise AND (&) operator compares two numbers on a bit level and returns a number where the bits of that number are turned on if the corresponding bits of both numbers are 1. For example:

 >  a:   00101010   42

> b:   00001111   15

 > a & b:   00001010   10


So remember, for every given bit in a and b:
```
0 & 0 = 0
0 & 1 = 0
1 & 0 = 0
1 & 1 = 1
```
######Parctice 2

Print out the result of calling bin() on 0b1110 & 0b101.
```
>>> print bin(0b1110 & 0b101)
0b100
```
---
**The bitwise OR (|) operator**

The bitwise OR (|) operator compares two numbers on a bit level and returns a number where the bits of that number are turned on if either of the corresponding bits of either number are 1. For example:

 > a:  00101010  42

 >b:  00001111  15

 >a | b:  00101111  47

So remember, for every given bit in a and b:
```
0 | 0 = 0
0 | 1 = 1
1 | 0 = 1
1 | 1 = 1
```

######Parctice 3

For practice, print out the result of using | on 0b1110 and 0b101 as a binary string. Try to do it on your own without using the | operator if you can help it.
```
>>> or_var=0b1110 | 0b101
>>>
>>> print or_var
15
>>> print bin(or_var)
0b1111
>>>

```
---
**The XOR (^) or exclusive or operator **

The XOR (^) or exclusive or operator compares two numbers on a bit level and returns a number where the bits of that number are turned on if either of the corresponding bits of the two numbers are 1, but not both.

>a:  00101010   42

>b:  00001111   15

>a ^ b:  00100101   37

So remember, for every given bit in a and b:
```
0 ^ 0 = 0
0 ^ 1 = 1
1 ^ 0 = 1
1 ^ 1 = 0
```
######Practice 4
For practice, print the result of using ^ on 0b1110 and 0b101 as a binary string. Try to do it on your own without using the ^ operator.
```
>>> xor= 0b1110 ^ 0b101
>>>
>>> print xor
11
>>> print bin(xor)
0b1011
>>>
```
---
** NOT (~)  bitwise operator**

The bitwise NOT operator (~) just flips all of the bits in a single number. What this actually means to the computer is actually very complicated, so we're not going to get into it. Just know that mathematically, this is equivalent to adding one to the number and then making it negative.
For example:
```
>>> print ~3
-4
>>> print ~42
-43
>>>
```

