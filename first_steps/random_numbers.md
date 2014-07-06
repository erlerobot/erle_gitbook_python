## Random numbers

The random module provides functions that generate pseudorandom numbers.
For using this module capabilities you should firts import it, with the syntxis:
```
from random import function
```

The most used random number generators are:
```
random.randint(a, b)
```
This returns a random integer N such that a <= N <= b.
The other is:
```
random.random()
```
The function random returns a random float between 0.0 and 1.0 (including 0.0
but not 1.0).

######Practice 1

Create two numbers: `num1`using randit and `num2`using random.Print them:
```
>>> from random import randint
>>> num1=randint(5,7)
>>> print num1
5
>>> from random import random
>>> num2=random()
>>> print num2
0.769876247837
>>>
```
