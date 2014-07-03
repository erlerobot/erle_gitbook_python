## Introduction: Function + lists

Functions can also take lists as inputs and perform various operations on those lists.In later chapter we will deepen in this topic.

For now,let's see an example to understand how it works:

######Practice 1

Write a function that counts how many times the string "fizz" appears in a list.

We create a count.py file with this content:

```
def fizz_count(x):
    count=0
    for item in x:
        if item == "fizz":
            count=count +1

    print count

fizz_count(["fizz","buzz"])
```
We execute it, the anwswer should be one:
```
root@erlerobot:~/Python_files# python count.py
1
root@erlerobot:~/Python_files#
```
