# Progressive Guide to Python Fundamentals

This guide is aimed at programmers who already have experience with other languages but are beginners in Python. The goal is to become familiar with the syntax and basic concepts of the language progressively.

## 1. Basic Concepts

### 1.1 Syntax and Basic Structure
- Indentation is mandatory instead of curly braces `{}`
- Use of `:` to define code blocks
- Case-sensitive language

```python
if True:
    print("Indentation is mandatory!")
```

### 1.2 Variables and Dynamic Typing
- Python does not require type declarations
- Types are inferred automatically

```python
x = 10       # Integer
y = 3.14     # Float
name = "Ana" # String
active = True # Boolean
```

### 1.3 Comments
- Single-line comment: `#`
- Multi-line comment: `""" ... """` or `''' ... '''`

```python
# This is a single-line comment
"""
This is a multi-line
comment
"""
```

## 2. Operators

### 2.1 Arithmetic Operators
```python
sum_ = 10 + 5
subtraction = 10 - 5
multiplication = 10 * 5
division = 10 / 3       # Returns float
int_division = 10 // 3  # Returns integer
modulus = 10 % 3        # Remainder of division
power = 2 ** 3          # Exponentiation
```

### 2.2 Logical and Comparison Operators
```python
result = (10 > 5) and (5 < 8)  # True
result = (10 == 5) or (5 != 8) # True
result = not (10 > 5)          # False
```

## 3. Control Structures

### 3.1 Conditionals
```python
x = 10
if x > 5:
    print("Greater than 5")
elif x == 5:
    print("Equal to 5")
else:
    print("Less than 5")
```

### 3.2 Loops
#### 3.2.1 `for`
```python
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4
```

#### 3.2.2 `while`
```python
x = 0
while x < 5:
    print(x)
    x += 1
```

## 4. Data Structures

### 4.1 Lists
```python
numbers = [1, 2, 3, 4]
numbers.append(5)
numbers.remove(2)
print(numbers)  # [1, 3, 4, 5]
```

#### 4.1.1 List Slicing
```python
lst = [0, 1, 2, 3, 4, 5]
print(lst[1:4])  # [1, 2, 3]
print(lst[:3])   # [0, 1, 2]
print(lst[3:])   # [3, 4, 5]
print(lst[::-1]) # [5, 4, 3, 2, 1, 0]
```

### 4.2 Tuples
```python
tuple_ = (1, 2, 3)
print(tuple_[0])  # 1
```

### 4.3 Dictionaries
```python
dictionary = {"name": "Ana", "age": 25}
print(dictionary["name"])  # Ana
dictionary["age"] = 26
```

### 4.4 Sets
```python
set_ = {1, 2, 3, 3}
print(set_)  # {1, 2, 3} (No duplicates)
```

### 4.5 String Manipulation
```python
text = "Hello, world!"
print(text.split(","))  # ['Hello', ' world!']
print("-".join(["Python", "is", "awesome"]))  # Python-is-awesome
print(text.replace("world", "Python"))  # Hello, Python!
```

## 5. Functions and Functional Programming

### 5.1 Function Definition
```python
def greeting(name):
    return f"Hello, {name}!"
print(greeting("Ana"))
```

### 5.2 Lambda Functions
```python
square = lambda x: x ** 2
print(square(4))  # 16
```

### 5.3 Map, Filter, and Reduce
```python
numbers = [1, 2, 3, 4]
double = list(map(lambda x: x * 2, numbers))  # [2, 4, 6, 8]
evens = list(filter(lambda x: x % 2 == 0, numbers))  # [2, 4]
```

## 6. File Handling
```python
with open("file.txt", "w") as file:
    file.write("Hello, world!")
```

## 7. Object-Oriented Programming (OOP)

### 7.1 Classes and Objects
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}"

person1 = Person("Ana", 25)
print(person1.greet())  # Hello, my name is Ana
```

## 8. Exception Handling
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Error: division by zero")
finally:
    print("Finally block always executes")
```

## 9. Modules and Packages

### 9.1 Importing Modules
```python
import math
print(math.sqrt(16))  # 4.0
```

### 9.2 Introduction to Packages and Libraries
- Using external packages like `numpy`, `pandas`, `requests`.
- Installing packages with `pip install <package>`.

```python
import requests
response = requests.get("https://api.github.com")
print(response.status_code)
```
