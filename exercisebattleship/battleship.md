## Battleship

In this project you will build a simplified, one-player version of the classic board game Battleship! In this version of the game, there will be a single ship hidden in a random location on a 5x5 grid. The player will have 10 guesses to try to sink the ship.

To build this game we will use our knowledge of lists, conditionals and functions in Python.

We will go step by step, given solutions  at the end you will find the solution(complete code stored in `battleship.py`).


####Ready? The computing starts here:

- Create a variable board and set it equal to an empty list.

- Create a 5 x 5 grid initialized to all 'O's and store it in board.
Tip:
```python
>>> board=["O"]*5
>>> print board
['O', 'O', 'O', 'O', 'O']
>>> print len(board)
5
````

 + Use `range()` to loop 5 times.
 + Inside the loop, `.append()` a list containing 5 "O"s to board, just like in the example above.
 + Note that these are capital letter "O" and not zeros.
 + Use the `print` command to display the contents of the board list.

**Solution1**:
```python
board=[]

for x in range(0,5):
    board.append(["O"]*5)

print board

```
- We can use the fact that our board is a list of lists to help us do this. Let's set up a for loop to go through each of the elements in the outer list (each of which is a row of our board) and print them.
 + First, delete your existing print statement.
Then, define a function named `print_board` with a single argument, board.
+ Inside the function, write a for loop to iterates through each row in board and print it to the screen.
+ Call your function with board to make sure it works.

**Solution 2**
```python

def print_board(board):
    for i in board:
        print i

print_board(board)
```
- Now we want to get rid of the commas, like this:
```
>>> letters = ['a', 'b', 'c', 'd']
>>> print " ".join(letters)
a b c d
>>>
```
 + Inside your function, inside your for loop, use " " as the separator to `.join` the elements of each row.

**Solution 3**
```python
def print_board(board):
    for row in board:
        print " ".join(row)

print_board(board)
```
- Now, let's hide our battleship in a random location on the board.Since we have a 2-dimensional list, we'll use two variables to store the ship's location, `ship_row` and `ship_col`.
Look at his example:
```python
>>> from random import randint
>>> coin = randint(0, 1)
>>> dice = randint(1, 6)
>>> print coin
0
>>> print dice
1
>>>
```
In the above example, we first import the `randint(low, high)` function from the random module.
Then, we generate either zero or one and store it in coin.
Finally, we generate a number from one to six inclusive.
Let's generate a `random_row` and `random_col` from zero to four.

 + Define two new functions, `random_row` and `random_col`, that each take board as input.
 + These functions should return a random row index and a random column index from your board, respectively. Use randint(0, len(board) - 1).
 + Call each function on board.

**Solution 4**
```python
def random_row(board):
    from random import randint
    return randint(0, len(board) - 1)

def random_col(board):
    from random import randint
    return randint(0, len(board) - 1)
```
- We are going to ask the user to guess the column and the row where our ship is stored:
 + Create a new variable called `guess_row and` set it to `int(raw_input("Guess Row: "))`.
 + Create a new variable called `guess_col` and set it to `int(raw_input("Guess Col: "))`.

- For now, while we're writing and debugging this part of the program, it will be helpful to know where that battleship is hidden. Let's add a print statement that displays the location of the hidden ship.We will delete it later on.
- We have the actual location of the ship and the player's guess so we can check to see if the player guessed right.For a guess to be right, `guess_col` should be equal to `ship_col` and `guess_row` should be equal to `ship_row`.
 + Add an else under the if "correct condition".
 + Print out "You missed my battleship!"
 + Set the list element at `guess_row`, `guess_col` to "X".
 + As the last line in your else statement, call `print_board(board)` again so you can see the "X".

**Solution 5**

```python
ship_row = random_row(board)
ship_col = random_col(board)
guess_row = int(raw_input("Guess Row:"))
guess_col = int(raw_input("Guess Col:"))

print ship_row
print ship_col

if guess_row==ship_row and guess_col==ship_col:
    print "Congratulations!You sank my battleship!"
else:
    print "You missed my battleship!"
    board[guess_row][guess_col]="X"
    print_board(board)
```

- Now let’s think a little bit more about the "miss" condition.

 + The user can enter a guess that's off the board.
 + He can guess a spot they’ve already guessed.
 + He can just miss the ship.
We'll add the first case:
 + Add a new if: statement that is nested under the else.
 + It should check if `guess_row` is not in range(5) or `guess_col` is not in range(5).
 + If that is the case, print out "Oops, that's not even in the ocean."
 + After your new if: statement, add an else: that contains your existing handler for an incorrect guess. Don't forget to indent the code.

- And now the second one:
 + Add an elif to see if the guessed location already has an 'X' in it.(board[col][row]=="X")
If it has, print "You guessed that one already."

**Solution 6**
```python
if guess_row==ship_row and guess_col==ship_col:
    print "Congratulations!You sank my battleship!"
else:
         if guess_col not in range(5) or  guess_row not in  range(5):
           print "Oops, that's not even in the ocean."
         elif board[guess_row][guess_col]=="X":
             print "You guessed that one already."

         else:

            print "You missed my battleship!"
            board[guess_row][guess_col]="X"
            print_board(board)

```


- We’d like our game to allow the player to make up to 4 guesses before they lose.We can use a `for` loop to iterate through a range. Each iteration will be a turn.

+ Add a `for` loop that repeats the guessing and checking part of your game for 4 turns.
+ At the beginning of each iteration, print "Turn", turn + 1 to let the player know what turn they are on.
+ Indent everything that should be repeated.

**Solution 7**
```python
for turn in range(4):


 guess_row = int(raw_input("Guess Row:"))
 guess_col = int(raw_input("Guess Col:"))

 if guess_row == ship_row and guess_col == ship_col:
    print "Congratulations! You sunk my battleship!"
 else:
    if (guess_row < 0 or guess_row > 4) or (guess_col < 0 or  guess_col > 4):
        print "Oops, that's not even in the ocean."
    elif(board[guess_row][guess_col] == "X"):
        print "You guessed that one already."
    else:
        print "You missed my battleship!"
        board[guess_row][guess_col] = "X"
    print "Turn:",turn+1
    print_board(board)
    ```


- If someone runs out of guesses without winning right now, the game just exits. It would be nice to let them know why.Since we only want this message to display if the user guesses wrong on their last turn, we need to think carefully about where to put it.
 + We’ll want to put it under the else that accounts for misses.
+ We’ll want to print the message no matter what the cause of the miss.
+ Since our turn variable starts at 0 and goes to 3, we will want to end the game when turn equals 3.

- We can use the command `break` to get out of a `for` loop, when the user guess the answer.
 + Add a `break` under the win condition to end the loop after a win.







