## Exercises: Control flow


######Exercise 1
Write a program to prompt the user for hours and rate per hour to compute gross pay.Take into account that the factory gives the employee 1.5 times the
hourly rate for hours worked above 40 hours.
```
Enter Hours: 45
Rate: 10
Pay: 475.0
```
######Exercise 2

*Pig Latin* is a language game, where you move the first letter of the word to the end and add "ay." So "Python" becomes "ythonpay." To write a Pig Latin translator in Python, here are the steps we'll need to take:
- Ask the user to input a word in English.
- Make sure the user entered a valid word.
- Convert the word from English to Pig Latin.
- Display the translation result.

First define a variable called `pyg`equal to "ay"  and ask the user to enter a word. Save the results of `raw_input()` in a variable called `original`.
Then add an `if `statement that checks that `len(original)` is greater than zero AND that the word the user enters contains only alphabetical characters(Note:`isalpha()` returns False since the string contains non-letter characters.). If the string actually has some characters in it, print the user's word.Otherwise (i.e. an else: statement), please print "empty".After that checks create a new variable called `word` that holds the `.lower()`-case conversion of `original`.
Create a new variable called `first` that holds `word[0], the first letter of word.
Create a new variable called `new_word` and set it equal to the concatenation of `word`, `first`, and `pyg`.Set `new_word` equal to the slice from the 1st index all the way to the end of `new_word`. Use `[1:len(new_word)]` to do this.

######Exercise 3

Write a program to prompt for a score between 0.0 and 1.0. If the core is out of range print an error. If the score is between 0.0 and 1.0, print a
grade using the following table:
```
Score Grade
>= 0.9 A
>= 0.8 B
>= 0.7 C
>= 0.6 D
< 0.6 F
```

######Exercise 4
Write a programm that ask for a number to the user and clasifies it:
```
number <2 SMALL
number <10 MEDIUM
number rest LARGE
```

##Solutions

######Exercise 1
```python
Enter worked hours:45
>>> hours=float(hours)
>>> rate=10
>>> if hours < 40:
...        pay=hours*rate
...        print "the pay is:", pay
... else:
...        pay = 40 * rate + (hours-40)*1.5*rate
...        print "the pay is:", pay
...
the pay is: 475.0
>>>
````

######Exercise 2
```python

pyg = 'ay'

original = raw_input('Enter a word:')

if len(original) > 0 and original.isalpha():
    print original
    word= original.lower()
    first=word[0]
    new_word= word +first +pyg
    new_word=new_word[1:len(new_word)]
else:
    print 'empty'
```

######Exercise 3
```python
>>> score=raw_input("Enter a score:")
Enter a score:0.79
>>> score=float(score)
>>> if score >=0.9:
...    print "A"
... elif score >= 0.8:
...    print "B"
... elif score >= 0.7:
...    print "C"
... elif score >=0.6:
...    print "D"
... elif score <= 0.6 :
...    print "F"
... else:
...    print "error"
...
C
>>>
```
######Exercise 4
```python
>>> num =raw_input ("Enter a number:")
Enter a number:6
>>> if num < 2:
...   print "SMALL"
... elif num < 10:
...   print "MEDIUM"
... else:
...   print "LARGE"
...
MEDIUM
>>>
```

