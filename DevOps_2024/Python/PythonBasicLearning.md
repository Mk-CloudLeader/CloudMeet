
### Table of Contents
  
 


[What is Python & key use cases of Python with AWS?](#what-is-python-and-key-use-cases-of-python-with-aws)


[Boto3Lab](#boto3lab)

[Commands](#commands)  

[Link](#link) 


### What is Python?
Python is a high-level, interpreted programming language renowned for its readability and simplicity. Its syntax emphasizes code clarity, making it an excellent choice for both beginners and experienced programmers. Python's versatility shines in various domains, including web development, data science, machine learning, and automation.

    - Key Use Cases of Python with AWS:
        - Infrastructure as Code (IaC)
        - Data Engineering and Analysis
        - Machine Learning and AI
        - Serverless Computing
        - Web Development
        - Automation and DevOps






### Python installation on Windows?

1. Download the Python Installer: Visit the official Python website:  https://www.python.org/downloads/windows/
    Choose the latest stable Python 3 release.   
    Download the executable installer.  

2. Run the Installer:

    Double-click the downloaded installer file (e.g., python-3.10.10-amd64.exe).
    Follow the on-screen instructions.
    Crucially, check the box that says "Add Python to PATH". This will make Python accessible from any command prompt or terminal.   

3. Verify Installation:

    Open a command prompt or PowerShell.   
    Type python --version and press Enter.
    If Python is installed correctly, you should see the installed Python version

```
$mukesh@Mukeshs-MBP% python3 --version
Python 3.12.4

```

###  Difference between Modules,package,library,function

**Modules**  - Contains Python code, Modules are used to organize and reuse code in Python. They can be imported into other Python files using the import statement.
A Python package is a directory containing Python modules. Packages are used to organize and distribute Python code. They can be installed into a Python environment using the pip package manager.
A Python library is a collection of Python modules and packages that are related to a particular topic or problem. Libraries can be used to provide functionality to Python programs without having to write that functionality from scratch.


- The main difference between a module, package, and library is their scope. A module is the **smallest** unit of code organization in Python. A package is a **collection** of related modules. A library is a **collection of packages and modules** that are related to a particular topic or problem.

- Another difference between a module, package, and library is how they are used. A module is imported into another Python file using the **import** statement. A package is installed into a Python environment using the **pip package manager**. A library can be used to provide functionality to Python programs without having to write that functionality from scratch.

**Example of module, package, and library**

Module:: math

Package:: numpy

Library:: scikit-learn

If you are new to Python, you might be confused about - libraries, packages, modules, and frameworks. From the context, these are some pieces of code but what’s the difference between them?
**Module** is the smallest piece of software. A module is a collection of methods or functions that are ready to be used elsewhere. 


```
Ex - Json
```
**Packages** are basically a directory of a collection of modules. Packages allow the hierarchical structure of the module namespace
    - There are a lot of built-in and open-source Python packages

```
    - ex : NumPy, pandas
 ```
- **Library** contains a collection of related modules and packages
```
- ex : PyTorch, Requests 
```

- **Frameworks** are a collection of modules and packages that help programmers to fast track the development process.
while libraries contain packages that perform specific operations, frameworks contain the basic flow and architecture of the application.
```
- ex : Django, Flash
```

# Python Basic Learning - Meetup-2024 

```
# Practice 1
- variables
- Numbers
- boolean
- string and string's method 

# Practice 2 
- list
- list's method
- dictonary, dictonary nested, dictonary's method  
- tuples 

# Practice 3
- comparators 
- boolean-operatiors

# Practice 4
- condition 
- while_loop
- breack_continue
- for_loop
- multiplelist
- range 

# Practice 5
- method
- built_in_functions


# Practice 6
- class
- class_inheritance

# Practice 7
- exceptionhandling 

# Practice 8 
- modules 

# Practice 9
- filedemo
```

### Practice 1 :variables, Numbers,boolean, string and string's method 

- Variables are containers for storing data values.
- A variable is created the moment you first assign a value to it.

```
x=5 
name = 'sudish'

a = b = c = 10

x, y, z=20,30,40
import keyword 


print( x )
print("x") # this will print x
print(name)
print(a)
print(b)
print(c)

print(x)
print(y)
print(z)
print(keyword.kwlist)

```

### Practice 2 :list,list's method,dictonary, dictonary nested, dictonary's method, tuples 

- Lists[] are used to store multiple items in a single variable.
- Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are Tuple, Set, and Dictionary, all with different qualities and usage.
- Lists are created using square brackets: ["a","b","c"]

- Dictionaries{} are used to store data values in key:value pairs.
- A dictionary is a collection which is ordered*, changeable and do not allow duplicates.
- dictionaries are created using curly brackets,: {"key1":"value1","key2:"value2"}

- Tuples () are used to store multiple items in a single variable.
- Tuple is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Set, and Dictionary, all with different qualities and usage.
- A tuple is a collection which is ordered and unchangeable.
- Tuples are written with round brackets ("a","c","c","d")

```
#List

name = ["Mukesh","Joe","John"] 
print(name)
cars = ["bmw", "swift","maruti"]  
City = ['Gaya', "nj", "nyc"]
print(cars,City)

print(cars[0])

print(cars[0:2])
print(cars[0],cars[1])


(name.append("Amit"))    # this will add new value 
print(name)       


# use of len in sting and List 
a =  "Mukesh kumar"

a = ["Mukesh", "kumar"]
print(len(a))

```

```
#Dictonary

cars = {"make":"BMW","module":'x3','year':2013}
print(cars["year"],cars["make"])
print(len(cars))

car={}
car['make'] = "bmw"
car['module'] = "x5"
car['year'] = 2024

print(car)
```

```
# Touple 
thistuple = ("apple", "banana", "cherry")
print(thistuple)

#Tuples allow duplicate values:
thistuple = ("apple", "banana", "cherry", "apple", "cherry")
print(thistuple)
print(len(thistuple))
```

### Practice 3: comparators, boolean-operatiors


### Practice 4 :condition, while_loop,breack_continue,for_loop,multiplelist,range 

- Condition : if, elif, else, neted if

    - if 
    -  elif :The elif keyword is Python's way of saying "if the previous conditions were not true, then try this condition" 
    - else : The else keyword catches anything which isn't caught by the preceding conditions.
    - Nested If : You can have if statements inside if statements, this is called nested if statements.

- Python Loops :Python has two primitive loop commands:
    -   while loops
    -   for loops

- For loops 
    - A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).
    - This is less like the for keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.
    - With the for loop we can execute a set of statements, once for each item in a list, tuple, set etc.

```
# EX-01

a = 33
b = 33

if b>a:
    print("b is greater than a")
elif a ==b:
    print("a and b both are bother")

```

```
#EX02:Else example 

a = 200
b = 33

if b > a:
    print("b is greater than a")
elif a ==b:
    print("a and b are equal")
else:
    print("a is greater than b")

color = "red"
if color == "green":
    print("yes")
else:
    print("no")
```


```
#Ex03: nested if

x =41
if x < 10:
    print("above ten,")
    if x > 20:
        print("and also above 20!")
    else:
        print("but not above 20.")
else:
    print("testing")

```

```
# EX04: while loop :Print i as long as i is less than 6:

i = 1
while i < 6:
    print(i)
    i += 1
```

```
# EX05:while loop : break 

i = 1
while i <6:
    print(i)
    if i == 3:
        break
    i +=1
```

```
# EX06: Continue :With the continue statement we can stop the current iteration, and continue with the next:

i = 0
while i < 6:
  print(i)   # 0 
  i += 1
#  if i == 3:
#    continue
  print(i)   # 1

----
i = 0
while i < 6:
#    print(i)
    if i ==3:
        continue
    i += 1
   
```


```
# EX07: else with while

i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")

```

```
# EX08 :how to combine sting and integer togther using "str" function 

x = 0
while x <= 10:
    
#    print("Value of x is: " +(str(x)))
    print("value oif x is:" ,x)
#    print(x)

#    x = x + 1
    x +=1


# 
l = [] 
num = 0
while num < 10:
    l.append(num)
    
#    print("Value of num is: " + str(num))
    print("Value of num is: ",num )
    print("*"*20)
    
    num += 1
    #num = num + 1

print(l)

```


```
# EX09: for loops 

for i in range(1, 21):
    if i % 5 == 0:
        continue
    #    break
    print(i)

------

fruits =["apple","banana","cherry"] 
for i in fruits:
    print(i)

------
fruits =["apple","banana","cherry"]
for i in fruits:
    if i == "banana":
        continue
    print(i)
```

```
#EX010: else in for loop 

for x in range(6):
    print(x)
else:
    print("finally finished")


```
### Practice 5 :method, built_in_functions

- Python Function : 
    - A function is a block of code which only runs when it is called.
    - You can pass data, known as parameters, into a function.
    - A function can return data as a result.
    - In Python a function is defined using the def keyword:

- Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.
    - def my_function(fname):
    - def my_function(fname,lname):

- Arbitrary Arguments, *args
    - If you do not know how many arguments that will be passed into your function, add a * before the parameter name in the function definition.
    - This way the function will receive a tuple of arguments, and can access the items accordingly:

```
# EX01 - Define new function 

def function():
    print("Vikas")
    print("mk")

function()

```
```
'''
def my_function(fname):
    print(fname + "Rfresh")

my_function("email")
my_function("To")
my_function("From")
'''
# with multiple arguments
def my_function(fname,lname,tname):
    print(fname + " " + lname + " " + tname)

my_function("Mukesh", "kumar", "pp")

```
```
def my_function(*kids):
 
    print("The youngest child is " + kids[3])

my_function("pp", "tt", "xx", "rr")

```

```
#Keyword Arguments :You can also send arguments with the key = value syntax.
# This way the order of the arguments does not matter.


def my_function(child3, child2, child1):
    print("The youngest child is " +child3)
my_function(child1="mk", child2="rr", child3="xx")

```
### Practice 7 :exceptionhandling 

- Exception Handling :When an error occurs, or exception as we call it, Python will normally stop and generate an error message.
    - These exceptions can be handled using the try statement:
- The try block lets you test a block of code for errors.
- The except block lets you handle the error.
- The else block lets you execute code when there is no error.
- The finally block lets you execute code, regardless of the result of the try- and except blocks.


```
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
```

### Practice 8  :modules 

- Consider a module to be the same as a code library.
- A file containing a set of functions you want to include in your application.

```
# create module , you need to save in file locally 
# created a file - mymodule.py


def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}

---
# call this from diffrent file 

import Basic_Learning.module.mymodule as mymodule   #location of local file 
mymodule.greeting("mk")                             # calling above module

```


### Practice 9 :filedemo

```
# update value of m_list in your local file 

my_list = [1, 2, 3]

my_file = open("firstfile.txt", "w")

for item in my_list:
    my_file.write(str(item) + "\n")

my_file.close()

```

### Boto3Lab

- Requirements
    * you must have AWS account 
    * Install the AWS SDK for Python (Boto3), Install the latest Boto 3 release via pip:
    ```
    pip install boto3
    ```
   * Configure your AWS access keys.
        * Important: For security, it is strongly recommend that you use IAM users instead of the root account for AWS access. 
        * Create IAM user and key key using $aws configure 
   
   ```
   aws_access_key_id = <YOUR_ACCESS_KEY_ID>
   aws_secret_access_key = <YOUR_SECRET_ACCESS_KEY>
   ```
   
- S3 examples : 
1. List all your buckets and send mail to your email ID 
2. Create bucket 

- Amazon CloudWatch examples
- Amazon DynamoDB
- Amazon EC2 examples
- AWS Identity and Access Management examples
- AWS Key Management Service (AWS KMS) examples
- AWS Secrets Manager
- Amazon SES examples
- Amazon SQS examples






### Commands 

```
- pip install <<packagename>>
- pip list |grep -i <packagename>
- pip show botocore - list detils information about installed package
- aws configure 

```


### Link


|AWS SDK for Python (Boto3)| https://aws.amazon.com/sdk-for-python/|

| AWS_API Ref| https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/index.html |

