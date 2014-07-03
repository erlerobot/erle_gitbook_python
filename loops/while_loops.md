## While loops

The `while` loop is similar to an if statement: it executes the code inside of it if some condition is true. The difference is that the `while` loop will continue to execute as long as the condition is **true**. In other words, instead of executing if something is true, it executes while that thing is true.


######Practice 1

We are going to use `while`and `if`to see the difference:
```
>>> count = 0
>>>
>>> if count < 10:
...     print "Hello, I am an if statement and count is", count
...
Hello, I am an if statement and count is 0
>>>

```
When using the following code we print the sentence 9 times(< is not the same as <=).Remember always to actualize the count, if not you get an infinite loop.
```
... while count < 10:
...     print "Hello, I am a while and count is", count
...     count += 1
...
Hello, I am a while and count is 0
Hello, I am a while and count is 1
Hello, I am a while and count is 2
Hello, I am a while and count is 3
Hello, I am a while and count is 4
Hello, I am a while and count is 5
Hello, I am a while and count is 6
Hello, I am a while and count is 7
Hello, I am a while and count is 8
Hello, I am a while and count is 9
>>>
````
######Practice 2
Create a while loop that prints out all the numbers from 1 to 10 squared (1, 4, 9, 16, ... , 100), each on their own line.
```
>>> num = 1
>>>
>>> while num<=10:  # Fill in the condition
...  print num**2    # Print num squared
...  num += 1 # Increment num (make sure to do this!)
...
1
4
9
16
25
36
49
64
81
100
>>>
```

 ######Practice 3
 A common application of a while loop is to check user input to see if it is valid. For example, if you ask the user to enter y or n and they instead enter 7, then you should re-prompt them for input.Analyze the code bellow:

 ```
>>> choice = raw_input('Enjoying the course? (y/n)')
Enjoying the course? (y/n) p
>>> while choice!="y" and choice !="n":  # Fill in the condition (before the colon)
...     choice = raw_input("Sorry, I didn't catch that. Enter again: ")
...
Sorry, I didn't catch that. Enter again: e
Sorry, I didn't catch that. Enter again: y
>>>
```







