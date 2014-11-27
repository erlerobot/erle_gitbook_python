## Advanced concepts about bitwise operators

A **bit mask** is just a variable that aids you with bitwise operations. A bit mask can help you turn specific bits on, turn others off, or just collect data from an integer about which bits are on or off.

Let's see an example:
######Practice 1
Define a function, `check_bit4, with one argument, input, an integer.
It should check to see if the fourth bit from the right is on.
If the bit is on, return "on" (not print!)
If the bit is off, return "off".
```python
>>> def check_bit4(input):
...     mask=0b1000
...     if input&mask >0:
...         return "on"
...     else:
...         return "off"
...
>>>
>>> check_bit4(0b1100)
'on'
>>>
```
---

You can also use masks to **turn a bit in a number on** using |. For example, let's say I want to make sure the rightmost bit of number a is turned on. I could do this:
```python
>>> a = 0b110 # 6
>>> mask = 0b1 # 1
>>> desired =  a | mask # 0b111, or 7
>>>
```
Using the bitwise | operator will turn a corresponding bit on if it is off and leave it on if it is already on.

Using the XOR (^) operator is very useful for **flipping bits**. Using ^ on a bit with the number one will return a result where that bit is flipped.

For example, let's say I want to flip all of the bits in a. I might do this:
```python
>>>
>>> a = 0b110 # 6
>>> mask = 0b111 # 7
>>> desired =  a ^ mask # 0b1
```

Finally, you can also use the left shift (<<) and right shift (>>) operators to slide masks into place.
```python
>>> a = 0b101
>>> # Tenth bit mask
...
>>> mask = (0b1 << 9)  # One less than ten
>>> desired = a ^ mask
```
Let's say that I want to turn on the 10th bit from the right of the integer a.

Instead of writing out the entire number, we slide a bit over using the << operator.

We use 9 because we only need to slide the mask nine places over from the first bit to reach the tenth bit.
