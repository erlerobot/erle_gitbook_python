## Asking the user for input

Sometimes we would like to take the value for a variable from the user via their
keyboard. Python provides a built-in function called `raw_input` that gets input from the keyboard (We will see fuctions later) .When this function is called, the program stops and waits forthe user to type something. When the user presses Return or Enter, the program
resumes and `raw_input` returns what the user typed as a **string**.

######Practice 1
We are going to make a programm that ask your name and your favorite color and shows a message.

We store this code into a file called Raw.py:

```

name = raw_input("What is your name?")
color = raw_input("What is your favorite color?")

print "Ah, so your name is %s and your favorite color is %s." % (name,  color)
```

Now we execute this file:
```
root@erlerobot:~# python Raw.py
What is your name? Paul
What is your favorite color? black
Ah, so your name is  Paul and your favorite color is  black.
root@erlerobot:~#
```

