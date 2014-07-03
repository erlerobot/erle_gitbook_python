## Exercises: List and Dictionaries

######Exercise 1
Given the following dictionary:
```
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

```
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


##Solutions

######Exercise 1
```
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

```
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
```
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
