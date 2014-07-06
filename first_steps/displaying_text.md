## Displaying values on the screen

For displaying a desired sentence os text on the scrren you should use a simple sintaxis, like the following one:

```python
print " Text goes here"
```
You can also display numbers and varibales:
```python
print number
```
```python
print varibale
```

The `,` character after our print statement means that our next print statement keeps printing on the same line.

######Practice 1

Create a file with a  "Hello world " message and
display it on the screen:
```
root@erlerobot:~# touch Hello.py
root@erlerobot:~# echo 'print "Hello World!"' > Hello.py
root@erlerobot:~# python Hello.py
Hello World!
root@erlerobot:~#
```
---
######Practice 2
Create a file containing three numbers and print them on the screen:

```
root@erlerobot:~/Python_files# touch Num.py
root@erlerobot:~/Python_files# echo 'print 1' >> Num.py
root@erlerobot:~/Python_files# echo 'print 4' >> Num.py
root@erlerobot:~/Python_files# echo 'print 6' >> Num.py
root@erlerobot:~/Python_files# python Num.py
1
4
6
```
---

######Practice 3

Display a variable on your screen:
```
root@erlerobot:~/Python_files# python
Python 2.7.3 (default, Sep 26 2013, 21:37:06)
[GCC 4.6.3] on linux2
Type "help", "copyright", "credits" or "license" for more information.
```
Like this you initialize the python program.

```python
>>> var="Hello"
>>> print "this is the variable: ", var
this is the variable: Hello

```

Notice that we have use the two methods of running Python.

