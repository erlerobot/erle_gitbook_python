## For loop

An alternative way to `while` loop is the `for` loop.
the `for` loop is looping through a known set of items so it runs through as many iterations as there are items in the set.

######Practice 1
Execute the following code and analyze the result:
```python
>>> friends = ['Joseph', 'Glenn', 'Sally']
>>>
>>> for friend in friends:
...    print 'Happy New Year:', friend
...    print 'Done!'
...
Happy New Year: Joseph
Done!
Happy New Year: Glenn
Done!
Happy New Year: Sally
Done!
>>>
```
---

**Enumerate**

A weakness of using this for-each style of iteration is that you don't know the index of the thing you're looking at. Generally this isn't an issue, but at times it is useful to know how far into the list you are. Thankfully the built-in `enumerate` function helps with this.

`enumerate` works by supplying a corresponding index to each element in the list that you pass it. Each time you go through the loop, index will be one greater, and item will be the next item in the sequence. It's very similar to using a normal for loop with a list, except this gives us an easy way to count how many items we've seen so far.

######Practice 2
Look the result of this code:

```python
>>> choices = ['pizza', 'pasta', 'salad', 'nachos']
>>>
>>> print 'Your choices are:'
Your choices are:
>>> for index, item in enumerate(choices):
...     print index, item
...
0 pizza
1 pasta
2 salad
3 nachos
>>>
```
---

**Zip**

It's also common to need to iterate over two lists at once. This is where the built-in `zip` function comes in handy.`zip` will create pairs of elements when passed two lists, and will stop at the end of the shorter list.`zip` can handle three or more lists as well.

######Practice 3
Compare each pair of elements and print the larger of the two.Print the biggest one of each pair.
```python
list_a = [3, 9, 17, 15, 19]
list_b = [2, 4, 8, 10, 30, 40, 50, 60, 70, 80, 90]
```
```
>>> for a, b in zip(list_a, list_b):
...
...     if a>b:
...         print a
...     else:
...         print b
...
...
3
9
17
15
30
>>>
```

---

**For/else**

Just like with `while`, for loops may have an else associated with them.That is the for/else loop.

In this case, the else statement is executed after the `for`, but only if the for ends normally—that is, not with a break.

######Practice 4
We have this fruit list:
```python
fruits = ['banana', 'apple', 'orange', 'tomato', 'pear', 'grape']
```
We are going to make a program that search for "carrot" between this fruit. If it doesn't appear it shows a succes message:

```python
>>> fruits = ['banana', 'apple', 'orange', 'tomato', 'pear', 'grape']
>>>
>>> print 'You have...'
You have...
>>> for f in fruits:
...     if f == 'carrot':
...         print 'A carrot is not a fruit!'
...         break
...     print 'A', f
... else:
...     print 'A fine selection of fruits!'
...
A banana
A apple
A orange
A tomato
A pear
A grape
A fine selection of fruits!
```
