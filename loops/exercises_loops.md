# Exercises: Loops

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
```
phrase = "A bird in the hand..."
```
- Do the following `for` each character in the phrase.
- If char is an 'A' or char is an 'a', print 'X', instead of char. Make sure to include the trailing comma.
- Otherwise (else:), please print char, with the trailing comma.


##Solutions

#####Exercise 1
Create a `random.py` file:
```
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
```
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
```
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


