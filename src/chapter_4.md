# Control Flow Statements

Control flow statements are essential in programming as they allow you to control the execution flow of your code based on certain conditions. In this tutorial section, we will cover the following control flow statements in Python 3.13:

- If-else conditions
- For loops
- While loops
- Break and continue statements

Let's dive into each of these concepts with explanations and examples.

## If-Else Conditions

Python uses the `if` statement to test conditions. If the condition is `True`, the subsequent block of code is executed. If the condition is `False`, the `else` block (if present) is executed. Additionally, `elif` (short for "else if") can be used to check multiple conditions.

```python
# Example of if-else conditions

age = 20

# Check if age is greater than or equal to 18
if age >= 18:
    print("You are an adult.")
else:
    print("You are not an adult.")

# Example of if-elif-else conditions

score = 75

# Check the range of the score and print corresponding grade
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

## For Loops

A `for` loop is used to iterate over a sequence (such as a list, tuple, dictionary, set, or string) and execute a block of code for each element in the sequence.

```python
# Example of for loop with a list

fruits = ["apple", "banana", "cherry"]

# Loop through each fruit in the list and print it
for fruit in fruits:
    print(fruit)

# Example of for loop with a range

# Loop through numbers 0 to 4 and print each number
for i in range(5):
    print(i)
```

## While Loops

A `while` loop is used to repeatedly execute a block of code as long as the specified condition is `True`.

```python
# Example of while loop

count = 0

# Loop while count is less than 5
while count < 5:
    print("Count:", count)
    count += 1  # Increment count
```

## Break and Continue Statements

The `break` statement is used to terminate the loop prematurely, while the `continue` statement is used to skip the current iteration and proceed to the next iteration of the loop.

```python
# Example of break statement in a for loop

numbers = [1, 2, 3, 4, 5]

for number in numbers:
    if number == 3:
        break  # Exit the loop when number is 3
    print(number)

# Example of continue statement in a for loop

for number in numbers:
    if number % 2 == 0:
        continue  # Skip the current iteration if number is even
    print(number)
```

In this tutorial section, we covered the basic control flow statements in Python 3.13: `if-else` conditions, `for` loops, `while` loops, and `break/continue` statements. These constructs are fundamental for creating logical and organized code. Experiment with these examples and practice writing your own control flow statements to get a better understanding.
