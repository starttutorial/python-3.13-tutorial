# Basics of Python Syntax

## Introduction
In this section, we will cover the basics of Python syntax. This includes variables, data types, operators, and basic input/output operations. Understanding these fundamental concepts is crucial for any programming task in Python.

## Variables
In Python, variables are used to store data values. You don't need to declare the type of a variable; Python infers it based on the value assigned.

```python
# Variables in Python
x = 5  # 'x' is an integer
y = "Hello"  # 'y' is a string
z = 3.14  # 'z' is a floating-point number

# Printing variables
print(x)  # Output: 5
print(y)  # Output: Hello
print(z)  # Output: 3.14
```

## Data Types
Python supports several data types, including integers, floats, strings, and booleans. Here's a brief overview of each:

### Integers
Whole numbers without a fractional part.

```python
a = 10  # Integer
```

### Floats
Numbers with a fractional part.

```python
b = 3.14159  # Float
```

### Strings
Sequences of characters enclosed in quotes.

```python
c = "This is a string"  # String
```

### Booleans
Represent truth values: `True` or `False`.

```python
d = True  # Boolean True
e = False  # Boolean False
```

## Operators
Operators are used to perform operations on variables and values. Python supports several types of operators:

### Arithmetic Operators
Used to perform mathematical operations.

```python
# Addition
sum = 5 + 3  # Output: 8

# Subtraction
difference = 10 - 2  # Output: 8

# Multiplication
product = 4 * 2  # Output: 8

# Division
quotient = 16 / 2  # Output: 8.0

# Floor Division
floor_div = 16 // 3  # Output: 5

# Modulus
remainder = 16 % 3  # Output: 1

# Exponentiation
power = 2 ** 3  # Output: 8
```

### Comparison Operators
Used to compare two values.

```python
# Equal
print(5 == 5)  # Output: True

# Not equal
print(5 != 3)  # Output: True

# Greater than
print(5 > 3)  # Output: True

# Less than
print(5 < 3)  # Output: False

# Greater than or equal to
print(5 >= 3)  # Output: True

# Less than or equal to
print(5 <= 3)  # Output: False
```

### Logical Operators
Used to combine conditional statements.

```python
# and operator
print(True and False)  # Output: False

# or operator
print(True or False)  # Output: True

# not operator
print(not True)  # Output: False
```

## Basic Input/Output Operations
Python provides simple functions for input and output operations.

### Output
The `print()` function is used to display output to the console.

```python
# Printing a simple message
print("Hello, World!")  # Output: Hello, World!

# Printing multiple items
print("The value of x is", x)  # Output: The value of x is 5
```

### Input
The `input()` function is used to take input from the user.

```python
# Taking input from the user
name = input("Enter your name: ")
print("Hello, " + name + "!")  # Output: Hello, [name]!

# Taking numerical input from the user
age = int(input("Enter your age: "))  # Convert input to an integer
print("You are", age, "years old.")  # Output: You are [age] years old.
```

This is the basic syntax you need to get started with Python. Understanding these concepts will help you build more complex programs in the future.
