## Importing functions

A module is a file that contains definitions—including variables and functions—that you can use once it is imported.There is a Python module named math that includes a number of useful variables and functions, and `sqrt()` is one of those functions. In order to access math, all you need is the import keyword. When you simply import a module this way, it's called a generic import.

Note: We have done this with `random`and with `datetime`.

To import a function (in this case `sqrt()` function) from this module follow the steps:
- Type `import math` .
- Insert `math.` before `sqrt()` so that it has the form `math.sqrt()`. This tells Python not only to import `math`, but to get the `sqrt()` function from within `math`.

Here you have an example:

```
>>> import math
>>> print math.sqrt(25)
5.0
```

It's possible to import only certain variables or functions from a given module. Pulling in just a single function from a module is called a function import, and it's done with the from keyword:
```
from module import function
```
For example:
```
>>> from math import sqrt
```

What if we still want all of the variables and functions in a module but don't want to have to constantly type `math.`?Universal import can handle this for you.
```
from module import *
```
Note:The `* `means all.
```
>>> from math import *
```

Universal imports may look great on the surface, but they're not a good idea for one very important reason: they fill your program with a ton of variable and function names without the safety of those names still being associated with the module(s) they came from.
If you have a function of your very own named sqrt and you import math, your function is safe: there is your sqrt and there is math.sqrt. If you do from math import *, however, you have a problem: namely, two different functions with the exact same name.

Even if your own definitions don't directly conflict with names from imported modules, if you import * from several modules at once, you won't be able to figure out which variable or function came from where.

This code will show you everything available in the `math` module.


```
>>> import math            # Imports the math module
>>> everything = dir(math) # Sets everything to a list of things from math
>>> print everything       # Prints 'em all!

['__doc__', '__file__', '__name__', '__package__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'hypot', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'trunc']
>>>
```


For these reasons, it's best to stick with either import module and type module.name or just import specific variables and functions from various modules as needed.
