
### Basic Syntax
```
# Variables and Data Types
x = 5               # Integer
y = 3.14            # Float
name = "Alice"      # String
is_valid = True     # Boolean

# Comments
# This is a single-line comment
""" 
This is a 
multi-line comment 
"""

# Printing Output
print("Hello, World!")
```
### Data Structures
```
# Lists
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # Add item
fruits[0]                # Access item
fruits[1] = "mango"      # Modify item
del fruits[2]            # Remove item

# Tuples (Immutable)
colors = ("red", "green", "blue")
colors[1]                # Access item

# Dictionaries (Key-Value Pairs)
person = {"name": "John", "age": 30}
person["name"]           # Access value
person["age"] = 31       # Modify value

# Sets
unique_numbers = {1, 2, 3, 4}
unique_numbers.add(5)    # Add item
unique_numbers.remove(3) # Remove item
```
### Control Structures
```
# Conditional Statements
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is equal to 10")
else:
    print("x is less than 10")

# Loops
# For Loop
for i in range(5):
    print(i)

# While Loop
count = 0
while count < 5:
    print(count)
    count += 1

# Loop Control
for i in range(10):
    if i == 5:
        break          # Exit loop
    if i % 2 == 0:
        continue       # Skip to next iteration
    print(i)
```
### Functions
```
# Defining Functions
def greet(name):
    return "Hello, " + name

# Function with Default Argument
def greet(name="Guest"):
    return "Hello, " + name

# Calling Functions
greeting = greet("Alice")
print(greeting)

# Lambda Functions (Anonymous Functions)
square = lambda x: x ** 2
print(square(5))
```
### Classes and Objects
```
# Defining a Class
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        return "Woof!"

# Creating an Object
my_dog = Dog("Buddy", 3)

# Accessing Object Properties
print(my_dog.name)  # Output: Buddy
print(my_dog.bark())  # Output: Woof!
```
### Modules and Packages
```
# Importing Modules
import math
print(math.sqrt(16))

# Importing Specific Functions from a Module
from math import pi, sqrt
print(pi)
print(sqrt(16))

# Creating a Module (Save this as mymodule.py)
def greet(name):
    return "Hello, " + name

# Importing a Custom Module
import mymodule
print(mymodule.greet("Alice"))
```

### File Handling
```
# Writing to a File
with open("file.txt", "w") as file:
    file.write("Hello, World!")

# Reading from a File
with open("file.txt", "r") as file:
    content = file.read()
    print(content)

# Appending to a File
with open("file.txt", "a") as file:
    file.write("\nWelcome to Python!")
```
### Exception Handling
```
try:
    x = 10 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")
finally:
    print("This will run no matter what.")
```

### List Comprehensions
```
# Basic List Comprehension
squares = [x ** 2 for x in range(10)]
print(squares)

# List Comprehension with Condition
evens = [x for x in range(10) if x % 2 == 0]
print(evens)
```

### Useful Functions
```
# Map Function
numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x ** 2, numbers))
print(squared)

# Filter Function
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)

# Zip Function
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]
combined = list(zip(names, ages))
print(combined)

# Enumerate Function
for index, value in enumerate(names):
    print(index, value)
```
### Common Libraries
```
# NumPy (Numerical Python)
import numpy as np
array = np.array([1, 2, 3, 4])
print(array.mean())

# Pandas (Data Manipulation)
import pandas as pd
data = pd.DataFrame({
    "Name": ["Alice", "Bob"],
    "Age": [25, 30]
})
print(data)

# Matplotlib (Plotting)
import matplotlib.pyplot as plt
plt.plot([1, 2, 3], [4, 5, 6])
plt.show()

# Requests (HTTP Requests)
import requests
response = requests.get("https://api.example.com/data")
print(response.json())
```
