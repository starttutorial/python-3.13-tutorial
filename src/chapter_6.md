# Functions

Functions are one of the fundamental building blocks in Python. They allow you to encapsulate reusable pieces of code, making your programs more modular, readable, and easier to maintain. In this section, we'll cover everything you need to know about functions in Python 3.13, including how to define them, use different types of function arguments, return values, and lambda functions.

## Defining Functions

A function in Python is defined using the `def` keyword, followed by the function name, parentheses containing any parameters, and a colon. The code block within every function starts with an indented line.

### Example:
```python
def greet(name):
    print(f"Hello, {name}!")
```

In this example, `greet` is a function that takes one argument, `name`, and prints a greeting.

## Function Arguments

Python functions can take different types of arguments:

1. **Positional Arguments**
2. **Keyword Arguments**
3. **Default Arguments**
4. **Variable-length Arguments**

### Positional Arguments
These are the most common type of arguments. Their values are assigned based on their position in the function call.

#### Example:
```python
def add(a, b):
    return a + b

result = add(3, 5)  # 3 and 5 are positional arguments
print(result)  # Output: 8
```

### Keyword Arguments
These specify the argument name in the function call and are assigned values based on the name.

#### Example:
```python
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

introduce(name="Alice", age=30)  # name and age are keyword arguments
```

### Default Arguments
You can provide default values for some parameters, which makes them optional in the function call.

#### Example:
```python
def greet(name, message="Hello"):
    print(f"{message}, {name}!")

greet("Alice")  # Output: Hello, Alice!
greet("Bob", "Hi")  # Output: Hi, Bob!
```

### Variable-length Arguments
These allow a function to accept an arbitrary number of arguments. There are two types:

- **Arbitrary Positional Arguments**: Use an asterisk `*` before the parameter name.
- **Arbitrary Keyword Arguments**: Use two asterisks `**` before the parameter name.

#### Example:
```python
def sum_all(*args):
    return sum(args)

print(sum_all(1, 2, 3, 4))  # Output: 10

def display_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=30, city="New York")
# Output:
# name: Alice
# age: 30
# city: New York
```

## Return Values

A function can return a value using the `return` statement. If no `return` statement is used, the function returns `None` by default.

### Example:
```python
def multiply(a, b):
    return a * b

result = multiply(4, 5)
print(result)  # Output: 20
```

## Lambda Functions

Lambda functions are small anonymous functions defined using the `lambda` keyword. They can take any number of arguments but have only one expression.

### Example:
```python
square = lambda x: x * x
print(square(5))  # Output: 25

add = lambda a, b: a + b
print(add(3, 5))  # Output: 8
```

Lambda functions are often used for short, throwaway functions or as arguments to higher-order functions like `map()`, `filter()`, and `sorted()`.

### Higher-order Functions Example:
```python
# Using lambda with map()
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x * x, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]

# Using lambda with filter()
filtered_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(filtered_numbers)  # Output: [2, 4]

# Using lambda with sorted()
people = [{'name': 'Alice', 'age': 30}, {'name': 'Bob', 'age': 25}]
sorted_people = sorted(people, key=lambda x: x['age'])
print(sorted_people)
# Output: [{'name': 'Bob', 'age': 25}, {'name': 'Alice', 'age': 30}]
```

This section should give you a comprehensive understanding of how to use functions in Python 3.13. With practice, you'll be able to create more modular and efficient programs.
