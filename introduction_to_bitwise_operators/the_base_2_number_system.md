## The Base 2 Number System

When we count, we usually do it in base 10. That means that each place in a number can hold one of ten values, 0-9. In binary we count in base two, where each place can hold one of two values: 0 or 1. The counting pattern is the same as in base 10 except when you carry over to a new column, you have to carry over every time a place goes higher than one (as opposed to higher than 9 in base 10).

For example, the numbers one and zero are the same in base 10 and base 2. But in base 2, once you get to the number 2 you have to carry over the one, resulting in the representation "10". Adding one again results in "11" (3) and adding one again results in "100" (4).

Contrary to counting in base 10, where each decimal place represents a power of 10, each place in a binary number represents a power of two (or a bit). The rightmost bit is the 1's bit (two to the zero power), the next bit is the 2's bit (two to the first), then 4, 8, 16, 32, and so on.

The binary number '1010' is 10 in base 2 because the 8's bit and the 2's bit are "on".
In Python, you can write numbers in binary format by starting the number with` 0b. When doing so, the numbers can be operated on like any other number.

That is :

|**-**|**-**|**-**|**-**|**system**|
|---|
|1|2|4|8|base 10|
|0/1|0/1|0/1|0/1|base 2|
|**Examples**|**-**|**-**|**-**|**-**|
|0|1|0|0|in base 10 is 2|
|0|1|0|1|in base 10 is 10|
|0|0|1|0|in base 10 is 4|
|1|0|1|0|in base 10 in 5|

In Python you have only to invert the values:

|**-**|**-**|**-**|**-**|**system**|
|---|
|8|4|2|1|base 10|
|**Examples**|**-**|**-**|**-**|**-**|
|0|0|1|0|in base 10 is 2|
|1|0|1|0|in base 10 is 10|

Here you ca find an example using Python:
```
>>> print 0b1,
1
>>> print 0b10,
2
>>> print 0b11,
3
>>> print 0b100,
4
>>> print 0b101,
5
>>> print 0b110,
6
>>> print 0b111
7
>>> print "******"
******
>>> print 0b1 + 0b11
4
>>> print 0b11 * 0b11
9
>>>
```

######Practice 1
Try to full-fill the values:
```
one = 0b1
two = 0b10
three = 0b11
four
five
six
seven
eight
nine
ten
eleven
twelve
```
Answer:
```
one = 0b0001
two = 0b0010
three = 0b0011
four = 0b0100
five = 0b0101
six = 0b0110
seven = 0b0111
eight = 0b1000
nine = 0b1001
ten = 0b1010
eleven = 0b1011
twelve = 0b1100
```
---

**bin()**

There are Python functions that can aid you with bitwise operations. In order to print a number in its binary representation, you can use the` bin()` function. `bin() `takes an integer as input and returns the binary representation of that integer in a string. (Keep in mind that after using the bin function, you can no longer operate on the value like a number.)

You can also represent numbers in base 8 and base 16 using the `oct() ` and `hex()` functions.

For example:
```
>>> print bin(1)
0b1 #This is a string!Be careful!
>>>
```

**int()**

Python has an `int() function that you've seen a bit of already. It can turn non-integer input into an integer.
What you might not know is that the `int` function actually has an optional second parameter.

```
>>> int("110", 2)
6

```
When given a string containing a number and the base that number is in, the function will return the value of that number converted to base ten.

######Practice 2

Print this code and analize the results:
```
print int("1",2)
print int("10",2)
print int("111",2)
print int("0b100",2)
print int(bin(5),2)
```
The results should be:
```
>>> print int("1",2)
1
>>> print int("10",2)
2
>>> print int("111",2)
7
>>> print int("0b100",2)
4
>>> print int(bin(5),2)
5
```

