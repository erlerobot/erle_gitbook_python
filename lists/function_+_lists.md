## Functions and lists

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
---
#####Passing a range into a function

The Python range() function is just a shortcut for generating a list, so you can use ranges in all the same places you can use lists.
```
range(6) # => [0,1,2,3,4,5]
range(1,6) # => [1,2,3,4,5]
range(1,6,3) # => [1,4]
```
The range function has three different versions:
```
range(stop)
range(start, stop)
range(start, stop, step)
```
In all cases, the range() function returns a list of numbers from start up to (but not including) stop. Each item Each item increases by step.If omitted, start defaults to zero and step defaults to one.

Now you can iterate through indexes:
```
for i in range(len(list)):
    print list[i]
    ```

This method is much safer. Since we aren't modifying the list.

######Practice 2

Create a function called total that adds up all the elements of an arbitrary list and returns that count, using the existing code as a hint. Use a for loop so it can be used for any size list.

```
>>> def total(numbers):
...   result=0
...   for number in range(len(numbers)):
...       result=result+numbers[number]
...
...   return result
...
>>> #Now we check if it works
...
>>> n = [3, 5, 7]
>>> total(n)
15
```
---
######Practice 3

Create a function that concatenates strings.
```
>>> def join_strings(words):
...     result=""
...     for i in words:
...         result=result + i
...     return result
...
>>> #Now we checkt if it works
...
>>> n = ["Michael", "Lieberman"]
>>> print join_strings(n)
MichaelLieberman
>>>
```
---
Note, if you analize the codes of practice 2 and 3: you can see how when working with numbers( `for elemt in list`) elemt takes the value:0,1,2... while when working with strings elemt takes the string in index 0,1,2.. value.
