## For loop with lists


If you want to do something with every item in the list, you can use a `for` loop. The command line is:
```
for variable in list_name:
```
A variable name follows the for keyword; it will be assigned the value of each list item in turn.

Then in `list_name `designates `list_nam`e as the list the loop will work on. The line ends with a colon (:) and the indented code that follows it will be executed once per item in the list.

######Practice 1
What does this code?
```
>>> my_list = [1,9,3,8,5,7]
>>>
>>> for number in my_list:
...     # Your code here
...     print number*2
...
...
```
The `for` loop will automatically execute your code as many times as there are items in my_list.The result is:
```
...
2
18
6
16
10
14
>>>
```

If your list is a jumbled mess, you may need to sort() it.Note that `.sort()` modifies the list rather than returning a new list.

######Practice 2
Write a `for`loop that iterates over `start_list = [5, 3, 1, 2, 4]` and `.append()s` each number squared (x ** 2) to `square_list`(initialized to empty list).
Then sort square_list.

```
>>> start_list = [5, 3, 1, 2, 4]
>>> square_list = []
>>>
>>>
>>> for number in start_list:
...    n=star_list[number-1]
...    square_list.append(n**2)
...
>>> #Now we reordenate the list
...
>>> square_list.sort()
>>> print square_list
[1, 4, 9, 16, 25]
>>>
over `start_list=[5, 3, 1, 2, 4] and .append()s each number squared (x ** 2) to `square_list` (which is initialized to empty list).
Then sort square_list.
```

######Practice 3
Use a `for` loop to print out all of the elements in the list names.
```
names = ["Adam","Alex","Mariah","Martine","Columbus"]
```
```
>>> names = ["Adam","Alex","Mariah","Martine","Columbus"]
>>>
>>> for name in names:
...    print name
...
Adam
Alex
Mariah
Martine
Columbus
>>>
```

You can also use the `for`loop with strings:
######Practice 4
We are going to print only the "i" letters for a string. Run this code and analyze what happend:

```

word = "Programming is fun!"

for letter in word:
    # Only print out the letter i
    if letter == "i":
        print letter
```
