## Loops basics

A loop is a sequence of instruction s that is continually repeated until a certain condition is reached.

For example `for `is  a loop :

```
>>> n=["Welcome", " to", " Erleboard", " world"]
>>> for x in n:
...   print x
...
Welcome
 to
 Erleboard
 world
>>>
```

This type of flow is called a loop because after the statements, in this case "print x" ,loops back around to the top. Each time we execute the body of the loop, we call it an iteration. For the
above loop, we would say, “It had four iterations” which means that the body of of
the loop was executed four times.

An endless source of amusement for programmers is the observation that the directions
on shampoo, “Lather, rinse, repeat,” are an infinite loop because there is
no iteration variable telling you how many times to execute the loop.

Sometimes you don’t know it’s time to end a loop until you get half way through
the body. In that case you can write an infinite loop on purpose and then use the
`break` statement to jump out of the loop(remember the battleship exercise).

######Practice 1
Analyze the code bellow:
```
>>> while True:
...     print count
...     count += 1
...     if count >= 10:
...         break
...
0
1
2
3
4
5
6
7
8
9
>>>
```
Note thet the while condition is always true, what leads to a infinite loop. See the effect of using `break`.


Something completely different about Python is the while/else construction. while/else is similar to if/else, but there is a difference: the else block will execute anytime the loop condition is evaluated to False. This means that it will execute if the loop is never entered or if the loop exits normally. If the loop exits as the result of a break, the else will not be executed.

######Practice 6

Copy this code in a file called `game.py`and  run it:
```
import random

print "Lucky Numbers! 3 numbers will be generated."
print "If one of them is a '5', you lose!"

count = 0
while count < 3:
    num = random.randint(1, 6)
    print num
    if num == 5:
        print "Sorry, you lose!"
        break
    count += 1
else:
    print "You win!"
```
