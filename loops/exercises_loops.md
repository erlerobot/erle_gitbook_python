## Exercises: Loops

######Exercise 1
Write a program that generates a random number (0-10) and ask you to guess it. You have three asserts.

- Define a random_number with randit between 0-10.
- Initialize `guesses_left` to 3.
- Use a while loop to let the user keep guessing so long as guesses_left is greater than zero.
- Ask the user for their guess, just like the second example above.
- If they guess correctly, print 'You win!' and break.
Decrement guesses_left by one.
- Use an else: case after your while loop to print:You lose.

###### Exercise 2
Create a for loop that prompts the user for a hobby 3 times, then appends each one to hobbies.

###### Exercise 3
REmember: The `,` character after our print statement means that our next print statement keeps printing on the same line.
Let's filter out the letter 'A' from our string.
```python
phrase = "A bird in the hand..."
```
- Do the following `for` each character in the phrase.
- If char is an 'A' or char is an 'a', print 'X', instead of char. Make sure to include the trailing comma.
- Otherwise (else:), please print char, with the trailing comma.


######Exercise 4
Define a function `is_even that` will take a number x as input.If x is even, then return True.
Otherwise, return False. Note: even means that is divisible by two.Check if it works.

######Exercise 5
Write a function called digit_sum that takes a positive integer n as input and returns the sum of all that number's digits.

######Exercise 6
Let's try a factorial problem.
To calculate the factorial of a non-negative integer x, just multiply all the integers from 1 through x. For example:
    3! is  equal to 1*2*3

######Exercise 7
Scrabble is a game where players get points by spelling words. Words are scored by adding together the point values of each individual letter.Define a function scrabble_score that takes a string word as input and returns the equivalent scrabble score for that word.
```python
score = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2,
         "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3,
         "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1,
         "r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4,
         "x": 8, "z": 10}
         ```

######Exercise 8

Define a function called count that has two arguments called sequence and item.
Return the number of times the item occurs in the list.For example: count([1,2,1,1], 1) should return 3 (because 1 appears 3 times in the list).

######Exercise 9

Write a function `remove_duplicates` that takes in a list and removes elements of the list that are the same.For example: remove_duplicates([1,1,2,2])
should return [1,2].

##Solutions

#####Exercise 1
Create a `random.py` file:
```python
from random import randint

# Generates a number from 1 through 10 inclusive
random_number = randint(1, 10)

guesses_left = 3
# Start your game!
while guesses_left>0:
    guess=int(raw_input("Enter your guess:"))
    if guess==random_number:
        print "You win"
        break
    guesses_left-=1
else:
    print "You lose"
```
And execute it.

######Exercise 2
```python
>>> hobbies = []
>>> for i in range(3):
...   hob=raw_input("Enter hobby:")
...   hobbies.append(hob)
...
Enter hobby:Shopping
Enter hobby:Swimming
Enter hobby:Golf
>>> print hobbies
['Shopping', 'Swimming', 'Golf']
>>>
```

######Exercise 3
```python
>>> phrase = "A bird in the hand..."
>>> for char in phrase:
...     if char == "A" or char == "a":
...         print "X",
...     else:
...         print char,
...
...
...
X   b i r d   i n   t h e   h X n d . . .
>>>
```

######Exercise 4
```python
>>> def is_even(x):
...     if x%2==0 :
...         return True
...     else:
...         return False
...
>>>
>>> is_even(7)
False
>>> is_even(8)
True
>>>
```
######Exercise 5
```python
>>> def digit_sum(n):
...     num=str(n)
...     count=0
...     for i in num:
...         add=int(i)
...         count=count+add
...
...     return count
...
>>>
>>> digit_sum(892)
19
>>>
```

######Exercise 6

```python
>>> def factorial(x):
...     count=1
...     for i in range(x):
...         count=count*(i+1)
...     return count
...
>>>
>>> factorial (12)
479001600
>>>
```
######Exercise 7
```python
>>> score = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2,
...          "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3,
...          "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1,
...          "r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4,
...          "x": 8, "z": 10}
>>>
... def scrabble_score(word):
...     word=word.lower()
...     total=0
...     for let in word:
...         total=score[let]+ total
...     return total
...
>>> scrabble_score("Hello")
8
>>>
>>>
```
######Exercise 8
```python
>>> def count(sequence,item):
...     total=0
...     for x in sequence:
...      if x==item:
...         total+=1
...     return total
...
>>>
>>> count([1,2,1,1,1,3],1)
4
>>>
```
######Exercise 9
```python
>>> def remove_duplicates(lst):
...     result = []
...     for item in lst:
...         if item not in result:
...             result.append(item)
...     return result
...
>>> remove_duplicates([1,1,3,4,5,6,6,7,7,8,3])
[1, 3, 4, 5, 6, 7, 8]
>>>
```
