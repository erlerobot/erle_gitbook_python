## Lists basics

Lists are a datatype you can use to store a collection of different pieces of information as a sequence under a single variable name. (Datatypes you've already learned about include strings, numbers, and booleans.)

You can assign items to a list with an expression of the form(with the items in between brackets):
```
list_name = [item_1, item_2]
```
A list can also be empty: empty_list = [].

Lists are very similar to strings, but there are a few key differences.

##### Accessing a list

You can access an individual item on the list by its index. An index is like an address that identifies the item's place in the list. The index appears directly after the list name, in between brackets, like this: list_name[index].

**List indices begin with 0, not 1!** You access the first item in a list like this: `list_name[0]`. The second item in a list is at index 1:` list_name[1]`.

######Practice 1
Make a list containg the zoo animals and print the 2nd. and the last one:


```
>>> zoo_animals = ["pangolin", "cassowary", "sloth","lion" ];
>>> print zoo_animals[1],zoo_animals[3]
cassowary lion
>>>
```
---
A list index behaves like any other variable name. It can be used to access as well as assign values.

######Practice 2
Write an assignment statement that will replace the item that currently holds the value "lion" in the `zoo_animals` list with another animal the tiger.
```
>>> zoo_animals[3]="tiger"
>>> print zoo_animals[3]
tiger
>>>
>>> print zoo_animals
['pangolin', 'cassowary', 'sloth', 'tiger']
>>>
```

Note that with the command `print list_name` you get printed the compelte list.
---
#####Adding elements to a list
A list doesn't have to have a fixed length. You can add items to the end of a list any time you like.

With the command `list_name.append('name')`you add a new item at the end of the list. With the command
`print len(list_name)`you can know how many items a list has.

######Practice 3

Add the 5th element to the list: "parrot". Display the number of list items and print the new list.
```
>>> zoo_animals.append("parrot")
>>> print len(zoo_animals)
5
>>> print zoo_animals
['pangolin', 'cassowary', 'sloth', 'tiger', 'parrot']
>>>
```
---
#####Extracting parts of a list
Sometimes, you only want to access a portion of a list.You should use this format command:
```
part_list=list_name[1:3]
```

######Practice 4
Given a list:
```
suitcase = ["sunglasses", "hat", "passport", "laptop", "suit", "shoes"]
```
- Create a list called `first` containing only the two first items from suitcase.
- Create a list called `middle` containing only the two middle items from suitcase.
- Create a list called `last` made up only of the last two items from suitcase.

```
>>> first  =suitcase[0:2]
>>> print first
['sunglasses', 'hat']
>>>
>>> middle =suitcase[2:4]
>>> print middle
['passport', 'laptop']
>>>
>>> last   =suitcase[4:6]
>>> print last
['suit', 'shoes']
>>>
```
---
##### Finding the index of a list element

You can use Use the `.index(item)` function to find the index of an element of the list.

######Practice 5
Given
```
animals = ["aardvark", "badger", "duck", "emu", "fennec fox"]
```
Use the `.index(item)` function to find the index of "duck".
Then `.insert(index, item)` the string "cobra" at that index.Print the result.
```
>>> animals = ["aardvark", "badger", "duck", "emu", "fennec fox"]
>>> print animals.index("duck")
2
>>> animals.insert(2,"cobra")
>>> print animals
['aardvark', 'badger', 'cobra', 'duck', 'emu', 'fennec fox']
>>>
```
---
##### Removing elements from a list

Sometimes you need to remove something from a list.
`n.pop(index)` will remove the item at index from the list and return it to you:
```
>>> n = [1, 3, 5]
>>> n.pop(1)
3
>>> print n
[1, 5]
```

`n.remove(item)` will remove the actual item if it finds it
```
>>> n = [1, 3, 5]
>>> n.remove(3)
>>> print n
[1, 5]
>>>
```

`del(n[1])` is like `.pop in that it will remove the item at the given index, but it won't return it:
```
>>> n=[1,3,5]
>>> del(n[0])
>>> print n
[3, 5]
```



######Practice 6
From the list below remove 'dagger', choose the command you like of the above ones:
```
backpack = ['xylophone', 'dagger', 'tent', 'bread loaf']
```
```
>>> backpack = ['xylophone', 'dagger', 'tent', 'bread loaf']
>>>
>>> backpack.remove('dagger')
>>> print backpack
['xylophone', 'tent', 'bread loaf']
>>>
```
