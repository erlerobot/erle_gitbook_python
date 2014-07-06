## Files basics

Until now, the Python code you've been writing comes from one source and only goes to one place: you type it in at the keyboard and its results are displayed in the console. But what if you want to read information from a file on your computer, and/or write that information to another file?

This process is called file *I/O* (the "I/O" stands for "input/output"), and Python has a number of built-in functions that handle this for you.

#####Opening a file
Let's walk through the process of writing to a file one step at a time.Let's analyze the follwing command:
```
f = open("output.txt", "w")
```
This told Python to open `output.txt` in "w" mode ("w" stands for "write"). We stored the result of this operation in a file object, f.

Doing this opens the file in write-mode and prepares Python to send data into the file.

You can open files in *write-only mode* ("w"), *read-only mode* ("r"), read and *write mode* ("r+"), and *append mode* ("a", which adds any new data you write to the file to the end of the file).

######Parctice 1
First you need to create a file on your site, called "output.txt" (If the file doesn't exists Python can't open it). You can do this easily from your terminal typing:
```
root@erlerobot:~/Python_files# touch output.txt
```

Create a variable, `my_file`, and set it equal to calling the open() function on `output.txt`. In this case, pass "r+" as a second argument to the function so the file will allow you to read and write to it.
Note: You should create a file `output.txt`.
```
my_file=open("output.txt","r+")
```
---
#####Writing on a file

Now it's time to write some data to our output.txt file.We can write to a Python file like so:
```
my_file.write("Data to be written")
```
The `write()` function takes a string argument, so we'll need to do a few things here:
You must close the file. You do this simply by calling `my_file.close() (we did this for you in the last exercise). If you don't close your file, Python won't write to it properly.


######Practice 2
Create a variables called `my_list` that contains
the squared numbers from 1 to 10.
Open yout `my_list`in "+r" mode and iterate over it to get each value.
Use `my_file.write()` to write each value to `output.txt`
Make sure to call `str()` on the iterating data so `.write()` will accept it
Make sure to add a newline ("\n") after each element to ensure each will appear on its own line.
Use `my_file.close()` to close the file when you're done.

```
>>> my_list = [i**2 for i in range(1,11)]
>>>
>>> my_file = open("output.txt", "r+")
>>>
>>>
>>> for num in my_list:
...     data=str(num)
...     my_file.write(data)
...     my_file.write("\n")
...
>>> my_file.close()
```
For now you don't know how to read the content in Python (is the next step), so if you  want to check the result display the content of the file  `output.txt` from your terminal like this this:
```
root@erlerobot:~/Python_files# cat output.txt
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
root@erlerobot:~/Python_files#
```
---

#####Reading a file

Finally, we want to know how to read from our output.txt file. As you might expect, we do this with the read() function, like so:
```
print my_file.read()
```

######Parctice 3

Declare a variable, `my_file`, and set it equal to the file object returned by calling `open()` with both "output.txt" and "r".
Next, print the result of using `.read()` on `my_file`, like the example above.
Make sure to `.close()` your file when you're done with it. All kinds of doom will happen if you don't.
```
>>> my_file=open("output.txt","r")
>>>
>>> print my_file.read()
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

>>> my_file.close()
```

---

What if we want to read from a file line by line, rather than pulling the entire file in at once. Thankfully, Python includes a `readline()` function that does exactly that.

If you open a file and call `.readline()` on the file object, you'll get the first line of the file; subsequent calls to `.readline()` will return successive lines.

######Practice 4

Create a file by using `touch text.txt` and edit it using `vi text editor`by typing `vi text.txt`.
```
root@erlerobot:~/Python_files# touch text.txt
root@erlerobot:~/Python_files# vi text.txt
```
Copy this content:

```
I'm the first line of the file!
I'm the second line.
Third line here, boss.
```

Declare a new variable `my_file` and store the result of calling `open()` on the "text.txt" file in "r"ead-only mode.
On three separate lines, print out the result of calling `my_file.readline()`. See how it gets the next line each time?
Don't forget to `close()` your file when you're done with it.

```
>>> my_file=open("text.txt","r")
>>>
>>> print my_file.readline()
"'m the first line of the file!\n"
>>>
>>> print my_file.readline()
"I'm the second line.\n"
>>>
>>> print my_file.readline()
'Third line here, boss.\n'
>>>
>>> my_file.close()
>>>
```
---
#####Closing files

We keep telling you that you **always need to close** your files after you're done writing to them.

During the I/O process, data is buffered: this means that it is held in a temporary location before being written to the file.

Python doesn't flush the buffer—that is, write data to the file—until it's sure you're done writing. One way to do this is to close the file. If you write to a file without closing, the data won't make it to the target file.

*Is there a way to get Python to automatically close our files for us?*

Yes, there is.You may not know this, but file objects contain a special pair of built-in methods: `__enter__()` and `__exit__()`. The details aren't important, but what is important is that when a file object's `__exit__()` method is invoked, it automatically closes the file. We invoke this method:Using `with` and `as`.

The syntax looks like this:
```
with open("file", "mode") as variable:
    # Read or write to the file
    ```


######Practice 5
Write any data you like to the `text.txt` file using `with...as`. Give your file object the usual name: `my_file.
```
>>> with open("text.txt","r+") as my_file:
...     my_file.write("Hey!I'm writing on the file!")
...     print my_file.read()
```

---

#####Checking if the file is closed

Finally, we'll want a way to test whether a file we've opened is closed. Sometimes we'll have a lot of file objects open, and if we're not careful, they won't all be closed. We can check it with:

```
f = open("bg.txt")
f.closed
# False
f.close()
f.closed
# True
```
Python file objects have a closed attribute which is True when the file is closed and False otherwise.

By checking `file_object.closed`, we'll know whether our file is closed and can call `close() on it if it's still open.

######Practice 6

Following with the code in Practice 5:
Check if the file is not `.closed`.
If that's the case, call `.close()` on it.
(You don't need an else here, since your if statement should do nothing if `.closed` is True.)
After your if statement, print out the value of `my_file.closed` to make sure your file is really closed.
```
>>> with open("text.txt","r+") as my_file:
...     my_file.write("Hey!I'm writing on the file!")
...     print my_file.read()
...

>>> f=open("text.txt")
>>> f.closed # If this returns True the file is closed, if not it is opened.
False
>>>
>>> if f.closed==True:
...  f.close()
...
>>>
>>>
>>> print my_file.closed
True
```


