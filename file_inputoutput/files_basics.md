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


