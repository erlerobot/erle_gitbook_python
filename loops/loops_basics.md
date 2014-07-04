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

**Break**

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
---

**Continue**

Another useful command is `continue`.Sometimes you are in an iteration of a loop and want to finish the current iteration and immediately jump to the next iteration. In that case you can use the ` continue`
statement to skip to the next iteration without finishing the body of the loop for
the current iteration.

######Practice 2

Here is an example of a loop that copies its input until the user types “done”, but
treats lines that start with the hash character as lines not to be printed (kind of like
Python comments).
Open a `cont.py`file and copy the code bellow:
```
while True:
  line = raw_input('> ')
  if line[0] == '#' :
   continue
  if line == 'done':
    break
print line
print 'Done!'
```
Here is a sample run of this new program with continue added.
```
root@erlerobot:~/Python_files# python cont.py
> hello there
hello there
> # don't print this
> print this!
print this!
> done
Done!
```
