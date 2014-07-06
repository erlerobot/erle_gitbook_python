## Exercises: List and Dictionaries

######Exercise 1
Given the following dictionary:
```python
inventory = {
    'gold' : 500,
    'pouch' : ['flint', 'twine', 'gemstone'],
    'backpack' : ['xylophone','dagger', 'bedroll','bread loaf']
}
```
Try to do the followings:
- Add a key to inventory called 'pocket'.
-  Set the value of 'pocket' to be a list consisting of the strings `'seashell', 'strange berry', and 'lint'`.
- `.sort() `the items in the list stored under the 'backpack' key.
- Then `.remove('dagger')` from the list of items stored under the 'backpack' key.
- Add 50 to the number stored under the 'gold' key.

######Exercise 2
Folow the steps bellow:
-Create a new dictionary called `prices` using `{}` format like the example above.
- Put these values in your `prices` dictionary:
```
"banana": 4,
"apple": 2,
"orange": 1.5,
"pear": 3
```
- Loop through each key in `prices`. For each key, print out the key along with its price and stock information. Print the answer in the following format:
```
apple
price: 2
stock: 0
```
- Let's determine how much money you would make if you sold all of your food.

 + Create a variable called `total` and set it to zero.
 + Loop through the prices dictionaries.For each key in prices, multiply the number in prices by the number in stock. Print that value into the console and then add it to total.
 + Finally, outside your loop, print total.

######Exercise 3

Follow the steps:

- First, make a list called groceries with the values "banana","orange", and "apple".
- Define this two dictionaries:

```python
stock = {
    "banana": 6,
    "apple": 0,
    "orange": 32,
    "pear": 15
}

prices = {
    "banana": 4,
    "apple": 2,
    "orange": 1.5,
    "pear": 3
}
```
- Define a function `compute_bill` that takes one argument food as input.
In the function, create a variable `total` with an initial value of zero.For each item in the food list, add the price of that item to total.
Finally, return the total.
Ignore whether or not the item you're billing for is in stock.Note that your function should work for any food list.
- Make the following changes to your compute_bill function:
 + While you loop through each item of food, only add the price of the item to total if the item's stock count is greater than zero.
 + If the item is in stock and after you add the price to the total, subtract one from the item's stock count.

######Exercise 4

This exercise is a bit more complicate. We will review all about list and dictionaries. The aim of this exercise is to make a gradebook for  teacher's  students.

Try to follow the steps:
- Create three dictionaries: `lloyd`, `alice`, and `tyler`.
- Give each dictionary the keys "name", "homework", "quizzes", and "tests".Have the "name" key be the name of the student (that is, lloyd's name should be "Lloyd") and the other keys should be an empty list.
Look in solutions, the "solution 1". Chechk if you have done it rigth.
- Now copy this code:
 ```python
lloyd = {
    "name": "Lloyd",
    "homework": [90.0,97.0,75.0,92.0],
    "quizzes": [88.0,40.0,94.0],
    "tests": [75.0,90.0]
}
alice = {
    "name": "Alice",
    "homework": [100.0, 92.0, 98.0, 100.0],
    "quizzes": [82.0, 83.0, 91.0],
    "tests": [89.0, 97.0]
}
tyler = {
    "name": "Tyler",
    "homework": [0.0, 87.0, 75.0, 22.0],
    "quizzes": [0.0, 75.0, 78.0],
    "tests": [100.0, 100.0]
}
```
- Below your code, create a list called `students `that contains `lloyd`, `alice`, and `tyler.
- for each student in your students list, print out that student's data, as follows:

 + print the student's name
 + print the student's homework
 + print the student's quizzes
 + print the student's tests

- Write a function average that takes a list of numbers and returns the average.

 + Define a function called average that has one argument, numbers.
 + Inside that function, call the built-in `sum()` function with the numbers list as a parameter. Store the result in a variable called total.
 + Use `float()` to convert total and store the result in total.
 + Divide total by the length of the numbers list. Use the built-in `len()` function to calculate that.
 + Return that result.

- Write a function called get_average that takes a student dictionary (like lloyd, alice, or tyler) as input and returns his/her weighted average.

 + Define a function called get_average that takes one argument called student.
 + Make a variable homework that stores the average() of student["homework"].
 + Repeat step 2 for "quizzes" and "tests".
 + Multiply the 3 averages by their weights and return the sum of those three. Homework is 10%, quizzes are 30% and tests are 60%.

- Define a new function called `get_letter_grade` that has one argument called score. Expect score to be a number.
 + Inside your function, test score using a chain of if: / elif: / else: statements, like so:
```
If score is 90 or above: return "A"
Else if score is 80 or above: return "B"
Else if score is 70 or above: return "C"
Else if score is 60 or above: return "D"
Otherwise: return "F"
```

 + Finally, test your function. Call your `get_letter_grade` function with the result of `get_average(lloyd)`. Print the resulting letter grade.

-Define a function called `get_class_average` that has one argument, students. You can expect students to be a list containing your three students.
 + First, make an empty list called results.
 + For each student item in the class list, calculate get_average(student) and then call results.append() with that result.
 + Finally, return the result of calling average() with results.

- Finally, print out the result of calling `get_class_average `with your students list. Your students should be [lloyd, alice, tyler].
- Then, print the result of `get_letter_grade` for the class's average.


##Solutions

######Exercise 1
```python
>>> inventory = {
...     'gold' : 500,
...     'pouch' : ['flint', 'twine', 'gemstone'],
...     'backpack' : ['xylophone','dagger', 'bedroll','bread loaf']
... }
>>>
>>> inventory['pocket']=['seashell', 'strange berry', 'lint']
>>>
>>> inventory['backpack'].sort()
>>>
>>> inventory['backpack'].remove('dagger')
>>>
>>> inventory['gold']=inventory['gold']+50
>>>
>>> print inventory
{'pocket': ['seashell', 'strange berry', 'lint'], 'backpack': ['bedroll', 'bread loaf', 'xylophone'], 'pouch': ['flint', 'twine', 'gemstone'], 'gold': 550}
>>>
```

######Exercise 2

Create and edit a `supermarket.py` file with `vi text editor` like this one:

```python
  1 #Create the prices dictionary:
  2 prices={}
  3 #Add values
  4 prices["banana"]=4
  5 prices["apple"]= 2
  6 prices["orange"]= 1.5
  7 prices["pear"]= 3
  8
  9 #Create the stock dictionary
 10 stock={}
 11 #Add values
 12 stock["banana"]= 6
 13 stock["apple"]= 0
 14 stock["orange"] =32
 15 stock["pear"]= 15
 16
 17 #Show all prices and stock
 18
 19 for food in prices:
 20     print food
 21     print "price: %s" % prices[food]
 22     print "stock: %s" % stock[food]
 23
 24 total=0
 25 for price in prices:
 26     money= prices[price]*stock[price]
 27     print money
 28     total=total +money
 29
 30 print "The total money is", total
 31
 ```
 Now, call the file using `python supermarket.py`:
```
root@erlerobot:~/Python_files# python supermarket.py
orange
price: 1.5
stock: 32
pear
price: 3
stock: 15
banana
price: 4
stock: 6
apple
price: 2
stock: 0
48.0
45
24
0
The total money is 117.0
root@erlerobot:~/Python_files#
```

######Exercise 3

Create a `shoplist.py`list with this content:
```python
shopping_list = ["banana", "orange", "apple"]

stock = {
    "banana": 6,
    "apple": 0,
    "orange": 32,
    "pear": 15
}

prices = {
    "banana": 4,
    "apple": 2,
    "orange": 1.5,
    "pear": 3
}


def compute_bill(food):
    total=0
    for x in food:
        price= prices[x]
        if stock[x]>0:
           total=total +price
           stock[x]=stock[x] -1
    print total

compute_bill(shopping_list)
```
Now execute the file with `python shoplist.py`:
```
root@erlerobot:~/Python_files# python shoplist.py
5.5
root@erlerobot:~/Python_files#
```

######Exercise 4

**Solution 1**

```python
lloyd = {
    "name": "Lloyd",
    "homework": [],
    "quizzes":[],
    "tests":[],
    }
alice = {"name": "Alice", "homework":[],"quizzes":[],"tests":[],}
tyler = {"name": "Tyler", "homework":[],"quizzes":[],"tests":[],}
```
**Solution complete*
Create `note.py`with this content:
```
lloyd = {
    "name": "Lloyd",
    "homework": [90.0, 97.0, 75.0, 92.0],
    "quizzes": [88.0, 40.0, 94.0],
    "tests": [75.0, 90.0]
}
alice = {
    "name": "Alice",
    "homework": [100.0, 92.0, 98.0, 100.0],
    "quizzes": [82.0, 83.0, 91.0],
    "tests": [89.0, 97.0]
}
tyler = {
    "name": "Tyler",
    "homework": [0.0, 87.0, 75.0, 22.0],
    "quizzes": [0.0, 75.0, 78.0],
    "tests": [100.0, 100.0]
}


students=[lloyd,alice,tyler]

for student in students:
    print student["name"]
    print student["homework"]
    print student["quizzes"]
    print student["tests"]

def average(numbers):
    total=sum(numbers)
    total=float(total)
    media= total/ (len(numbers))
    return media

def get_average(student):
    homework=average(student["homework"])
    quizzes=average(student["quizzes"])
    tests=average(student["tests"])
    final=0.1*homework +0.3*quizzes + 0.6*tests
    return final

def get_letter_grade(score):
    if score >= 90:
        return "A"
    elif score >=80:
        return "B"
    elif score >=70:
        return "C"
    elif score >=60:
        return "D"
    else:
        return "F"

print get_letter_grade(get_average(lloyd))




def get_class_average(students):
      results=[]
      for student in students:
          r=get_average(student)
          results.append(r)

      return average(results)


students=[lloyd,alice,tyler]

print get_class_average(students)

print get_letter_grade(get_class_average(students))
    ```
Execute the file with `python note.py`:
```
root@erlerobot:~/Python_files# python note.py
Lloyd
[90.0, 97.0, 75.0, 92.0]
[88.0, 40.0, 94.0]
[75.0, 90.0]
Alice
[100.0, 92.0, 98.0, 100.0]
[82.0, 83.0, 91.0]
[89.0, 97.0]
Tyler
[0.0, 87.0, 75.0, 22.0]
[0.0, 75.0, 78.0]
[100.0, 100.0]
B
83.8666666667
B
root@erlerobot:~/Python_files#
```
