## Lambdas

Python supports the creation of anonymous functions (i.e. functions that are not bound to a name) at runtime, using a construct called "lambda".

This is one of the more powerful aspects of Python, that it allows for a style of programming called functional programming, which means that you're allowed to pass functions around just as if they were variables or values. Sometimes we take this for granted, but not all languages allow this.

Let's see a pair of examples:

Typing
```python
lambda x: x % 3 == 0
```
Is the same as
```python
def by_three(x):
    return x % 3 == 0
```
Only we don't need to actually give the function a name; it does its work and returns a value without one. That's why the function the lambda creates is an anonymous function.

Another expample of the use of lambda function:
```python
>>> my_list = range(16)
>>> print filter(lambda x: x % 3 == 0, my_list)
[0, 3, 6, 9, 12, 15]
```
When we pass the lambda to `filter`, filter uses the lambda to determine what to filter, and the second argument (my_list, which is just the numbers 0 – 15) is the list it does the filtering on.

Take into account that if you plan on creating a function you'll use over and over, you're better off using `def` and giving that function a name.

######Practice 1

We have this piece of code:

```python
languages = ["HTML", "JavaScript", "Python", "Ruby"]
print filter(_______, _______)
```

- Fill in the first part of the filter function with a lambda. The lambda should ensure that only "Python" is returned by the filter.
- Fill in the second part of the filter function with languages, the list to filter.

Remember, `filter() `takes two arguments: the first is the function that tells it what to filter, and the second is the object to perform the filtering on.

```python
>>> languages = ["HTML", "JavaScript", "Python", "Ruby"]
>>> print filter(lambda word: word=="Python", languages)
['Python']
>>>
```
