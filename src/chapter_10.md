# File Handling

File handling is an essential skill in Python that allows you to create, read, update, and delete files. This section will guide you through the basic operations involving file handling in Python 3.13.

## Opening Files

To open a file in Python, you use the `open()` function, which returns a file object. The `open()` function requires a filename and a mode.

### File Opening Modes

- `'r'`: Read mode (default). Opens the file for reading.
- `'w'`: Write mode. Opens the file for writing (creates a new file if it doesn't exist or truncates the file if it does).
- `'a'`: Append mode. Opens the file for appending (creates a new file if it doesn't exist).
- `'x'`: Exclusive creation mode. Creates a new file and returns an error if it already exists.
- `'b'`: Binary mode (used in conjunction with other modes, e.g., `'rb'` or `'wb'`).
- `'t'`: Text mode (default).

Let's start with an example of opening a file in read mode:

```python
# Open a file named 'example.txt' in read mode
file = open('example.txt', 'r')

# Always ensure to close the file after completing operations
file.close()
```

## Reading Files

There are several methods to read the contents of a file:

- `read()`: Reads the entire file.
- `readline()`: Reads a single line from the file.
- `readlines()`: Reads all the lines and returns them as a list.

### Example of Reading a File

```python
# Open the file in read mode
file = open('example.txt', 'r')

# Read the entire file
content = file.read()
print(content)

# Close the file
file.close()
```

### Example of Reading Line by Line

```python
# Open the file in read mode
file = open('example.txt', 'r')

# Read and print each line
for line in file:
    print(line, end='')

# Close the file
file.close()
```

## Writing to Files

To write to a file, you can use the `write()` or `writelines()` methods. Remember to open the file in write (`'w'`) or append (`'a'`) mode.

### Example of Writing to a File

```python
# Open the file in write mode
file = open('example.txt', 'w')

# Write a string to the file
file.write("Hello, World!\n")

# Close the file
file.close()
```

### Example of Appending to a File

```python
# Open the file in append mode
file = open('example.txt', 'a')

# Append a string to the file
file.write("Appending a new line.\n")

# Close the file
file.close()
```

## Closing Files

It's crucial to close the file after completing your operations to free up system resources. This is done using the `close()` method.

### Example of Closing a File

As shown in the examples above, always remember to call `file.close()` after you're done with reading or writing.

## Using the `with` Statement

To ensure that files are properly closed after their suite finishes, Python provides the `with` statement. This can be particularly useful as it automatically handles closing the file, even if exceptions occur.

### Example Using `with` Statement

```python
# Open and read the file using 'with' statement
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)

# No need to call file.close() explicitly
```

By using the `with` statement, you ensure that the file is closed properly without needing to call `close()` manually.

## Summary

To summarize, file handling in Python involves:
1. Opening a file using the `open()` function.
2. Performing operations like reading or writing.
3. Closing the file using the `close()` method or by using the `with` statement to handle it automatically.

These basic operations provide the foundation for more complex file manipulations. Remember to always handle files with care to avoid data corruption or loss.
