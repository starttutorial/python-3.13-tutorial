# Error Handling

Error handling is a crucial aspect of writing robust and reliable Python code. Python provides a flexible framework for handling exceptions, which are runtime errors that can potentially crash your program if not managed properly. This section will cover the use of `try`, `except`, `else`, and `finally` blocks, as well as how to raise exceptions and create custom exceptions. We will illustrate these concepts with examples to help you understand their practical applications.

## The `try` and `except` Blocks

The `try` block lets you test a block of code for errors. The `except` block enables you to handle the error. Here's a basic structure:

```python
try:
    # Code that might cause an exception
    risky_operation()
except SpecificException as e:
    # Code that runs if a specific exception occurs
    print(f"An error occurred: {e}")
```

For example:

```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Cannot divide by zero: {e}")
```

**Output:**

```
Cannot divide by zero: division by zero
```

## The `else` Block

The `else` block can be used to define code that executes if no exceptions were raised in the `try` block.

```python
try:
    result = 10 / 2
except ZeroDivisionError as e:
    print(f"Cannot divide by zero: {e}")
else:
    print(f"Division successful, result is {result}")
```

**Output:**

```
Division successful, result is 5.0
```

## The `finally` Block

The `finally` block allows you to execute code, regardless of whether an exception was raised or not. This is useful for cleanup actions like closing files or releasing resources.

```python
try:
    file = open('example.txt', 'r')
    content = file.read()
except FileNotFoundError as e:
    print(f"File not found: {e}")
finally:
    file.close()
    print("File closed")
```

Even if an exception occurs, the `finally` block will execute and ensure the file is closed:

**Output:**

```
File not found: [Errno 2] No such file or directory: 'example.txt'
File closed
```

## Raising Exceptions

Sometimes you might want to raise an exception intentionally, using the `raise` keyword.

```python
def check_positive(number):
    if number < 0:
        raise ValueError("Number must be positive")
    return number

try:
    check_positive(-5)
except ValueError as e:
    print(f"Error: {e}")
```

**Output:**

```
Error: Number must be positive
```

## Creating Custom Exceptions

Python allows you to define your own exceptions by creating a new exception class. Custom exceptions should inherit from the base `Exception` class.

```python
class CustomError(Exception):
    """Base class for other exceptions"""
    pass

class ValueTooSmallError(CustomError):
    """Raised when the input value is too small"""
    pass

class ValueTooLargeError(CustomError):
    """Raised when the input value is too large"""
    pass

# Example usage
def test_value(value):
    if value < 10:
        raise ValueTooSmallError("Value is too small")
    elif value > 100:
        raise ValueTooLargeError("Value is too large")
    else:
        return "Value is within the acceptable range"

try:
    test_value(5)
except ValueTooSmallError as e:
    print(f"Error: {e}")
except ValueTooLargeError as e:
    print(f"Error: {e}")
```

**Output:**

```
Error: Value is too small
```

In this example, we defined a base class `CustomError` and two derived classes `ValueTooSmallError` and `ValueTooLargeError`. These custom exceptions provide more specific error messages and improve code readability.

## Summary

- **`try` block**: Contains code that might throw an exception.
- **`except` block**: Handles specific exceptions that might be raised in the `try` block.
- **`else` block**: Executes if no exceptions are raised in the `try` block.
- **`finally` block**: Executes code regardless of whether an exception was raised or not.
- **`raise` keyword**: Used to raise an exception intentionally.
- **Custom exceptions**: User-defined exceptions that provide more specific error details.

Understanding and implementing proper error handling ensures your Python programs can gracefully manage unexpected situations, improving the robustness and reliability of your code.
