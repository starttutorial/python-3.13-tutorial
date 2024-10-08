# Data Structures

In Python, data structures are used to store and organize data efficiently. The most commonly used data structures in Python are lists, tuples, sets, and dictionaries. Each of these data structures has unique characteristics and use-cases. In this section, we will explore each of these data structures with examples of how to use them.

## Lists

Lists are ordered collections of items that are mutable (modifiable). They can contain items of different data types.

```python
# Creating a list
fruits = ["apple", "banana", "cherry"]
print(fruits)  # Output: ['apple', 'banana', 'cherry']

# Accessing elements
print(fruits[1])  # Output: banana

# Modifying elements
fruits[1] = "blueberry"
print(fruits)  # Output: ['apple', 'blueberry', 'cherry']

# Adding elements
fruits.append("orange")
print(fruits)  # Output: ['apple', 'blueberry', 'cherry', 'orange']

# Removing elements
fruits.remove("cherry")
print(fruits)  # Output: ['apple', 'blueberry', 'orange']
```

## Tuples

Tuples are ordered collections of items that are immutable (cannot be modified). They are useful for storing data that should not change.

```python
# Creating a tuple
colors = ("red", "green", "blue")
print(colors)  # Output: ('red', 'green', 'blue')

# Accessing elements
print(colors[0])  # Output: red

# Attempting to modify elements (This will raise an error)
# colors[1] = "yellow"  # Uncommenting this line will raise a TypeError

# Tuples can be used for unpacking
r, g, b = colors
print(r, g, b)  # Output: red green blue
```

## Sets

Sets are unordered collections of unique items. They are used to store elements where order does not matter, and duplicates are not allowed.

```python
# Creating a set
numbers = {1, 2, 3, 4}
print(numbers)  # Output: {1, 2, 3, 4}

# Adding elements
numbers.add(5)
print(numbers)  # Output: {1, 2, 3, 4, 5}

# Removing elements
numbers.remove(4)
print(numbers)  # Output: {1, 2, 3, 5}

# Sets are useful for set operations like union, intersection, and difference
odd_numbers = {1, 3, 5, 7}
even_numbers = {2, 4, 6, 8}

union_set = odd_numbers.union(even_numbers)
print(union_set)  # Output: {1, 2, 3, 4, 5, 6, 7, 8}

intersection_set = numbers.intersection(odd_numbers)
print(intersection_set)  # Output: {1, 3, 5}
```

## Dictionaries

Dictionaries are collections of key-value pairs. They are unordered, and each key is unique. Dictionaries are often used to store data that can be looked up by a key.

```python
# Creating a dictionary
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
print(person)  # Output: {'name': 'Alice', 'age': 30, 'city': 'New York'}

# Accessing values
print(person["name"])  # Output: Alice

# Modifying values
person["age"] = 31
print(person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'New York'}

# Adding key-value pairs
person["profession"] = "Engineer"
print(person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'New York', 'profession': 'Engineer'}

# Removing key-value pairs
del person["city"]
print(person)  # Output: {'name': 'Alice', 'age': 31, 'profession': 'Engineer'}

# Iterating over dictionary items
for key, value in person.items():
    print(key, value)
# Output:
# name Alice
# age 31
# profession Engineer
```

By understanding and utilizing these data structures, you can efficiently manage and manipulate data in your Python programs. Each data structure has its advantages and appropriate use-cases, so it's important to choose the right one for your specific needs.
