# Python Programming Notes

A clear, corrected, and structured introduction to Python programming.

## Topics covered

1. Introduction to Python
2. Printing and comments
3. Variables and naming rules
4. Data types and type conversion
5. User input
6. Operators
7. Conditional statements
8. Loops
9. Lists, tuples, sets, and dictionaries
10. Functions
11. Practice programs

## 1. Introduction to Python

Python is a high-level, interpreted, general-purpose programming language.

- **High-level:** Its syntax is comparatively easy for humans to read.
- **Interpreted:** Python executes instructions through an interpreter.
- **Object-oriented:** Python supports classes and objects.
- **Case-sensitive:** `name`, `Name`, and `NAME` are treated as different identifiers.

```python
print("Hello, everyone!")
print("Welcome to Python programming.")
```

## 2. Printing Output

The `print()` function displays text, numbers, and calculated results.

Text values must be placed inside single or double quotation marks.

```python
print("Hello")
print('Python')
print(10)
print(5 + 3)
```

### Python is case-sensitive

The correct function name is `print()`, not `Print()`.

The following incorrect statement is shown as a comment so that the notebook remains executable:

```python
Print("Hello")  # NameError
```

```python
print("This statement works correctly.")

# Incorrect:
# Print("This causes a NameError because Python is case-sensitive.")
```

## 3. Comments

Comments explain code and are ignored by Python.

- A single-line comment begins with `#`.
- Triple-quoted strings are sometimes used for multi-line notes, although they are technically string literals.

```python
# This is a single-line comment.
print("Python ignores the comment above.")

multi_line_note = '''
This is a multi-line string.
It can be used to store text across several lines.
'''
print(multi_line_note)
```

## 4. Variables

A variable is a named container that stores a value.

Python creates a variable when a value is assigned using the `=` operator.

```python
x = 10
y = 20

total = x + y

print("x =", x)
print("y =", y)
print("Sum =", total)
```

### Variable naming rules

A variable name:

- Must begin with a letter or underscore.
- Cannot begin with a number.
- May contain letters, numbers, and underscores.
- Cannot contain spaces or symbols such as `@`, `#`, or `-`.
- Cannot be a Python keyword.
- Is case-sensitive.

Use meaningful names such as `student_name` rather than unnecessarily long or unclear names.

```python
student_name = "Jayashree"
_age = 18
graduation_year = 2030
course1 = "Python"

print(student_name, _age, graduation_year, course1)
```

Examples of invalid variable names:

```python
8name = "Amit"       # Begins with a number
student name = "Amit" # Contains a space
price@item = 50       # Contains @
class = "Python"      # `class` is a keyword
```

## 5. Data Types

Common built-in Python data types include:

| Data type | Description | Example |
|---|---|---|
| `int` | Whole number | `10`, `-6` |
| `float` | Decimal number | `3.14`, `9.5` |
| `str` | Text | `"Amit"` |
| `bool` | Logical value | `True`, `False` |
| `complex` | Complex number | `5 + 9j` |

Use `type()` to identify the data type of a value.

```python
integer_value = -100
float_value = 5.5
string_value = "Amit"
boolean_value = True
complex_value = 5 + 9j

print(type(integer_value))
print(type(float_value))
print(type(string_value))
print(type(boolean_value))
print(type(complex_value))
```

Invalid values such as `5 + 2m` or `True12.5` are not valid Python syntax.

A complex number uses `j`, for example `5 + 2j`.

```python
valid_complex_number = 5 + 2j
print(valid_complex_number)
print(type(valid_complex_number))
```

## 6. User Input

The `input()` function reads data entered by the user.

By default, `input()` always returns a string. Convert it when a numeric value is required.

```python
# Run this cell and enter your name.
name = input("Enter your name: ")
print("Hello,", name)
print("Data type:", type(name))
```

```python
# Run this cell and enter your age.
age = int(input("Enter your age: "))
print("Next year, you will be", age + 1)
print("Data type:", type(age))
```

### Type conversion

Type conversion changes a value from one data type to another.

Common conversion functions:

- `int()` converts to an integer.
- `float()` converts to a floating-point number.
- `str()` converts to a string.
- `bool()` converts to a Boolean value.

```python
text_number = "1000"
integer_number = int(text_number)
decimal_number = float(integer_number)
converted_text = str(decimal_number)

print(text_number, type(text_number))
print(integer_number, type(integer_number))
print(decimal_number, type(decimal_number))
print(converted_text, type(converted_text))
```

### Boolean conversion

The following values normally convert to `False`:

- `0`
- `0.0`
- `""` (empty string)
- Empty containers such as `[]`, `{}`, and `()`
- `None`

Most other values convert to `True`.

```python
print(bool(0))
print(bool(""))
print(bool(100))
print(bool(" "))
print(bool(1))
```

## 7. Operators

Operators perform calculations and comparisons.

### Arithmetic operators

| Operator | Meaning |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `//` | Floor division |
| `%` | Remainder |
| `**` | Exponentiation |

```python
a = 10
b = 6

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor division:", a // b)
print("Remainder:", a % b)
print("Exponent:", a ** b)
```

### Comparison operators

Comparison operators return either `True` or `False`.

```python
num1 = 100
num2 = 50

print(num1 > num2)
print(num1 < num2)
print(num1 == num2)
print(num1 != num2)
print(num1 >= num2)
print(num1 <= num2)
```

### Assignment operators

Assignment operators update a variable's current value.

```python
value = 50
print("Initial value:", value)

value += 30
print("After += 30:", value)

value -= 10
print("After -= 10:", value)

value *= 2
print("After *= 2:", value)

value /= 4
print("After /= 4:", value)
```

### Logical operators

- `and` returns `True` only when both conditions are true.
- `or` returns `True` when at least one condition is true.
- `not` reverses a Boolean value.

```python
print(True and False)
print(True and True)
print(True or False)
print(not True)
print(not False)
```

## 8. Conditional Statements

Conditional statements execute different blocks of code according to conditions.

Python uses indentation to identify the statements belonging to an `if`, `elif`, or `else` block.

```python
a = int(input("Enter the first number: "))
b = int(input("Enter the second number: "))

if a > b:
    print("The first number is greater.")
elif b > a:
    print("The second number is greater.")
else:
    print("Both numbers are equal.")
```

### Even or odd number

```python
number = int(input("Enter a number: "))

if number % 2 == 0:
    print("The number is even.")
else:
    print("The number is odd.")
```

### Nested conditions

A nested `if` statement is an `if` statement placed inside another condition.

```python
age = int(input("Enter age: "))
gender = input("Enter gender: ").strip().lower()

if age >= 18:
    print("The person is an adult.")

    if gender == "male":
        print("The person is an adult male.")
    elif gender == "female":
        print("The person is an adult female.")
    else:
        print("Gender was not entered as male or female.")
else:
    print("The person is a minor.")
```

### Student examination eligibility and grade

```python
attendance = float(input("Enter attendance percentage: "))
marks = float(input("Enter marks out of 100: "))

if attendance < 75:
    print("Not allowed to take the examination.")
else:
    if marks >= 90:
        print("Grade: O")
    elif marks >= 75:
        print("Grade: A")
    elif marks >= 60:
        print("Grade: B")
    elif marks >= 40:
        print("Grade: C")
    else:
        print("Grade: F")
```

### Voting eligibility in India

```python
age = int(input("Enter age: "))
country = input("Enter country: ").strip().lower()

if age >= 18 and country == "india":
    print("Eligible to vote in India.")
else:
    print("Not eligible to vote in India.")
```

### Simple calculator

```python
num1 = float(input("Enter the first number: "))
operator = input("Enter an operator (+, -, *, /): ").strip()
num2 = float(input("Enter the second number: "))

if operator == "+":
    print("Result:", num1 + num2)
elif operator == "-":
    print("Result:", num1 - num2)
elif operator == "*":
    print("Result:", num1 * num2)
elif operator == "/":
    if num2 == 0:
        print("Division by zero is not allowed.")
    else:
        print("Result:", num1 / num2)
else:
    print("Invalid operator.")
```

### Leap-year checker

```python
year = int(input("Enter a year: "))

if year % 400 == 0:
    print(year, "is a leap year.")
elif year % 100 == 0:
    print(year, "is not a leap year.")
elif year % 4 == 0:
    print(year, "is a leap year.")
else:
    print(year, "is not a leap year.")
```

### Basic login example

```python
correct_username = "admin"
correct_password = "password123"

username = input("Enter username: ")
password = input("Enter password: ")

if username == correct_username and password == correct_password:
    print("Login successful.")
else:
    print("Incorrect username or password.")
```

## 9. Loops

Loops repeatedly execute a block of code.

- Use a `for` loop when iterating over a sequence or a known range.
- Use a `while` loop while a condition remains true.

### `for` loop and `range()`

```python
for number in range(1, 11):
    print(number)
```

`range(start, stop, step)` excludes the `stop` value.

For example, `range(1, 11)` produces values from 1 through 10.

```python
for number in range(10, 0, -2):
    print(number)
```

### `while` loop

```python
number = 1

while number <= 10:
    print(number)
    number += 1
```

### Sum of numbers from 2 through 11

```python
total = 0

for number in range(2, 12):
    total += number

print("Sum:", total)
```

### Product of numbers from 5 through 15

```python
product = 1

for number in range(5, 16):
    product *= number

print("Product:", product)
```

### `break` and `continue`

- `break` immediately terminates a loop.
- `continue` skips the current iteration and proceeds to the next one.

```python
print("Using continue:")
for number in range(1, 11):
    if number == 4:
        continue
    print(number)

print("\nUsing break:")
for number in range(1, 11):
    if number == 6:
        break
    print(number)
```

## 10. Python Containers

Python provides several built-in container types:

- List
- Tuple
- Set
- Dictionary

### Lists

A list is:

- Ordered
- Mutable
- Able to contain duplicate values
- Able to contain different data types

Lists use square brackets: `[]`.

```python
items = [1, 2, 3, 4.5, "Python", True]

print(items)
print(type(items))
print("Length:", len(items))
```

### List indexing

Positive indexing begins at `0`.

Negative indexing begins at `-1`, which refers to the last element.

```python
items = [10, 20, 30, 40, 50, 60]

print("First item:", items[0])
print("Third item:", items[2])
print("Last item:", items[-1])
print("Second-last item:", items[-2])
```

### List slicing

The syntax is:

```python
list_name[start:stop:step]
```

The `stop` index is excluded.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(numbers[2:7])
print(numbers[:5])
print(numbers[5:])
print(numbers[::2])
print(numbers[::-1])
```

### Common list methods

- `append(value)` adds a value at the end.
- `insert(index, value)` inserts a value at a specified position.
- `pop()` removes and returns an item.
- `remove(value)` removes the first matching value.
- `count(value)` counts occurrences.

```python
names = ["Amit", "Riya", "Python"]

names.append("Shyam")
names.insert(1, "Kritika")
print("After additions:", names)

removed_item = names.pop()
print("Popped item:", removed_item)

names.remove("Python")
print("Final list:", names)
print("Count of Amit:", names.count("Amit"))
```

### Tuples

A tuple is ordered but immutable. Its elements cannot be reassigned after creation.

Tuples use parentheses: `()`.

```python
coordinates = (10, 20, 30)

print(coordinates)
print(coordinates[1])
print(type(coordinates))

# Invalid because tuples are immutable:
# coordinates[1] = 100
```

### Sets

A set:

- Stores unique values
- Is unordered
- Does not support indexing
- Is mutable

Sets use curly braces: `{}`.

```python
values = {10, 20, 20, 30, 30, 30}

print(values)

values.add(40)
values.remove(20)

print(values)
```

### Set operations

```python
set_a = {1, 2, 3, 4, 5}
set_b = {4, 5, 6, 7, 8}

print("Union:", set_a.union(set_b))
print("Intersection:", set_a.intersection(set_b))
print("Difference:", set_a.difference(set_b))
```

### Dictionaries

A dictionary stores data as `key: value` pairs.

- Keys must be unique.
- Values may be duplicated.
- A value is accessed using its key.

```python
players = {
    "Sehwag": 78,
    "Dhoni": 88,
    "Yuvraj": 93,
    "Virat": 105,
    "Rohit": 264
}

print(players)
print("Virat's score:", players["Virat"])
print("Keys:", players.keys())
print("Values:", players.values())
print("Items:", players.items())
```

## 11. Functions

A function is a reusable block of code that performs a particular task.

A function is defined using `def` and executed by calling its name.

```python
def add_four_numbers(num1, num2, num3, num4):
    return num1 + num2 + num3 + num4

result = add_four_numbers(10, 29, 30, 25)
print("Sum:", result)
```

### Parameters and arguments

- A **parameter** is a variable written in the function definition.
- An **argument** is the actual value supplied when calling the function.

```python
def greet(name):
    print("Hello,", name)

greet("Vansh")
greet("Taufik")
```

### Function to check whether a number is even or odd

```python
def check_even_or_odd(number):
    if number % 2 == 0:
        return "Even"
    return "Odd"

print(check_even_or_odd(10))
print(check_even_or_odd(7))
```

### Function to calculate the average of four numbers

```python
def calculate_average(num1, num2, num3, num4):
    total = num1 + num2 + num3 + num4
    return total / 4

print(calculate_average(4, 10, 12, 16))
```

### Multiplication table function

```python
def print_table(number):
    for multiplier in range(1, 11):
        print(f"{number} × {multiplier} = {number * multiplier}")

print_table(5)
```

### Find the greatest of three numbers

```python
def greatest_of_three(a, b, c):
    if a >= b and a >= c:
        return a
    if b >= a and b >= c:
        return b
    return c

print("Greatest number:", greatest_of_three(25, 80, 60))
```

## 12. Practice Programs

### First 50 natural numbers

The following program:

1. Creates a list of the first 50 natural numbers.
2. Counts the even numbers.
3. Finds the sum.
4. Reverses the list.

```python
numbers = list(range(1, 51))
even_count = sum(1 for number in numbers if number % 2 == 0)
total_sum = sum(numbers)
reversed_numbers = numbers[::-1]

print("Numbers:", numbers)
print("Even-number count:", even_count)
print("Sum:", total_sum)
print("Reversed:", reversed_numbers)
```

### Factorial using a loop

```python
def factorial(number):
    if number < 0:
        raise ValueError("Factorial is not defined for negative numbers.")

    result = 1
    for value in range(1, number + 1):
        result *= value
    return result

print("5! =", factorial(5))
```

### Count vowels in a string

```python
def count_vowels(text):
    vowels = "aeiouAEIOU"
    count = 0

    for character in text:
        if character in vowels:
            count += 1

    return count

print(count_vowels("Python Programming"))
```

### Reverse an integer

```python
def reverse_number(number):
    sign = -1 if number < 0 else 1
    reversed_digits = str(abs(number))[::-1]
    return sign * int(reversed_digits)

print(reverse_number(12345))
print(reverse_number(-908))
```

### Factorial using recursion

```python
def recursive_factorial(number):
    if number < 0:
        raise ValueError("Factorial is not defined for negative numbers.")
    if number <= 1:
        return 1
    return number * recursive_factorial(number - 1)

print(recursive_factorial(5))
```

### Fibonacci series

```python
def fibonacci(count):
    if count < 0:
        raise ValueError("Count cannot be negative.")

    sequence = []
    first, second = 0, 1

    for _ in range(count):
        sequence.append(first)
        first, second = second, first + second

    return sequence

print(fibonacci(10))
```
