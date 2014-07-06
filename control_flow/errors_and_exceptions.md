##  Errors and Exceptions

Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. Errors detected during execution are called exceptions and are not unconditionally fatal.It is possible to write programs that handle selected exceptions.

We use `try`and `except`to avoid this errors. Let's see an example:
```python
>>> num=4
>>> if num<10:
...  try:
...   num=num**3
...   print num
...  except:
...   print "Error"
...
64
>>>
>>> num = "Hola"
>>>
>>> if num<10:
...  try:
...   num=num**3
...   print num
...  except:
...   print "Error"
...
Error
```
If `try`is executed successfully the `except`is ignored. If `try`fails, the `except`is executed.

######Practice 1

Write a program that ask for an integer number. `while True` use `try`to ask this number and then `break` if the value is not correct, print an error message.

The code syntaxis is the following. Copy this in `pra.py`file:
```python
while True:
 try:
  num=int(raw_input("Enter an integer number:")

  break
 except ValueError:
  print"That is not a valid number!Try again..."
 ```
 The execution result on this:

 ```
 root@erlerobot:~/Python_files# python pra.py
 Enter an integer number:9.8
 That is not a valid number!Try again...
 Enter an integer number:9
 root@erlerobot:~/Python_files#
 ```


