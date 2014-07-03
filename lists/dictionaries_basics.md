## Dictionaries basics

A dictionary is similar to a list, but you access values by looking up a key instead of an index. A key can be any string or number. Dictionaries are enclosed in curly braces, like so:
```
d = {'key1' : 1, 'key2' : 2, 'key3' : 3}
```
This is a dictionary called d with three key-value pairs. The key 'key1' points to the value 1, 'key2' to 2, and so on.

Dictionaries are great for things like phone books (pairing a name with a phone number), login pages (pairing an e-mail address with a username)...

#####Accessing a dictionary

Note that accessing dictionary values by key is just like accessing list values by index.

######Practice 1
Given this dictinary:
```
residents = {'Puffin' : 104, 'Sloth' : 105, 'Burmese Python' : 106}
```
Print the value stored under the 'Sloth' key:
```
>>> residents = {'Puffin' : 104, 'Sloth' : 105, 'Burmese Python' : 106}
>>> print residents['Sloth']
105

```


#####Adding elements to a dictionary

Like Lists, Dictionaries are "mutable". This means they can be changed after they are created. One advantage of this is that we can add new key/value pairs to the dictionary after it is created like so:
```
dict_name[new_key] = new_value
```
An empty pair of curly braces `{}` is an empty dictionary, just like an empty pair of` [] `is an empty list.

The length `len()` of a dictionary is the number of key-value pairs it has. Each pair counts only once, even if the value is a list. (That's right: you can put lists inside dictionaries!)

######Practice 2
Add three elements to `menu{}`.
Print the number of elements in menu and the menu itselfs.
```
>>> menu = {} # Empty dictionary
>>> menu['Sunday']=16.78
>>> print menu['Sunday']
16.78
>>> menu['Monday']=6.78
>>> print menu['Monday']
6.78
>>> menu['Tuesday']= 9.98
>>> print menu['Tuesday']
9.98
>>>
>>> print "There are " + str(len(menu)) + " items on the menu."
There are 3 items on the menu.
>>> print menu
{'Sunday': 16.78, 'Tuesday': 9.98, 'Monday': 6.78}
>>>
```
#####Removing elements from a dictionary and associating values with keys.

Because dictionaries are mutable, they can be changed in many ways. Items can be removed from a dictionary with the del command:
```
del dict_name[key_name]
```
will remove the key key_name and its associated value from the dictionary.

A new value can be associated with a key by assigning a value to the key, like so:
```
dict_name[key] = new_value
```

######Practice 3
Given the dictionary:
```
# key - animal_name : value - location
zoo_animals = { 'Unicorn' : 'Cotton Candy House',
'Sloth' : 'Rainforest Exhibit',
'Bengal Tiger' : 'Jungle House',
'Atlantic Puffin' : 'Arctic Exhibit',
'Rockhopper Penguin' : 'Arctic Exhibit'}
```
- Delete the 'Sloth' and 'Bengal Tiger' items from zoo_animals using `del`.

- Set the value associated with 'Rockhopper Penguin' to anything other than 'Arctic Exhibit.

```
>>> zoo_animals = { 'Unicorn' : 'Cotton Candy House',
... 'Sloth' : 'Rainforest Exhibit',
... 'Bengal Tiger' : 'Jungle House',
... 'Atlantic Puffin' : 'Arctic Exhibit',
... 'Rockhopper Penguin' : 'Arctic Exhibit'}
>>>
>>> del zoo_animals['Sloth']
>>> del zoo_animals['Bengal Tiger']
>>> print zoo_animals
{'Atlantic Puffin': 'Arctic Exhibit', 'Rockhopper Penguin': 'Arctic Exhibit', 'Unicorn': 'Cotton Candy House'}
>>>
>>> zoo_animals['Rockhopper Penguin']='Arctic Dance'
>>> print zoo_animals
{'Atlantic Puffin': 'Arctic Exhibit', 'Rockhopper Penguin': 'Arctic Dance', 'Unicorn': 'Cotton Candy House'}
>>>

```


