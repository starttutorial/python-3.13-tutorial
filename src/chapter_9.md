# Working with Python Modules and Packages

Python modules and packages are fundamental aspects of writing efficient and organized code. This section explains how to create, import, and use Python modules and packages with practical examples.

## What is a Module?

A module in Python is a file containing Python definitions and statements. The file name is the module name with the suffix `.py` added. Modules allow you to logically organize your Python code. Grouping related code into a module makes the code easier to understand and use.

### Creating a Module

To create a module, you simply write Python code and save it with a `.py` extension. For example, let's create a module named `mymodule.py`.

```python
# mymodule.py

def greet(name):
    return f"Hello, {name}!"

def add(a, b):
    return a + b
```

### Importing a Module

To use the functions and variables defined in a module, you need to import it using the `import` statement.

```python
# main.py

import mymodule

print(mymodule.greet("Alice"))  # Output: Hello, Alice!
print(mymodule.add(5, 3))       # Output: 8
```

You can also import specific functions or variables from a module:

```python
# main.py

from mymodule import greet, add

print(greet("Bob"))  # Output: Hello, Bob!
print(add(10, 2))    # Output: 12
```

## What is a Package?

A package is a way of structuring Python’s module namespace by using "dotted module names". A package is a directory that contains a special file called `__init__.py` and can contain multiple modules or sub-packages.

### Creating a Package

To create a package, follow these steps:

1. Create a directory for the package.
2. Create an `__init__.py` file inside the directory (this file can be empty, but it must be present).
3. Add modules inside the package directory.

Let's create a package named `mypackage` with the following structure:

```
mypackage/
    __init__.py
    math_operations.py
    string_operations.py
```

Here are the contents of the modules:

`math_operations.py`:
```python
# math_operations.py

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

`string_operations.py`:
```python
# string_operations.py

def uppercase(s):
    return s.upper()

def lowercase(s):
    return s.lower()
```

### Importing from a Package

You can import modules from a package using the `import` statement or `from ... import ...` statement.

```python
# main.py

from mypackage import math_operations, string_operations

print(math_operations.add(4, 5))       # Output: 9
print(string_operations.uppercase("hello"))  # Output: HELLO
```

You can also import specific functions from the modules within a package:

```python
# main.py

from mypackage.math_operations import add
from mypackage.string_operations import uppercase

print(add(10, 20))            # Output: 30
print(uppercase("python"))    # Output: PYTHON
```

### Using `__all__` in Packages

The `__init__.py` file can be used to define the `__all__` variable, which specifies the modules to be imported when `from package import *` is used.

`__init__.py`:
```python
# __init__.py

__all__ = ["math_operations", "string_operations"]
```

Now, you can import all specified modules from the package:

```python
# main.py

from mypackage import *

print(math_operations.add(15, 5))       # Output: 20
print(string_operations.lowercase("PYTHON"))  # Output: python
```

## Conclusion

Modules and packages in Python provide a way to organize and reuse code efficiently. By creating modules, you can encapsulate related functions and variables, and by structuring them into packages, you can manage large codebases more effectively. This tutorial covered the basics of creating, importing, and using modules and packages in Python 3.13, along with practical examples to help you get started.
