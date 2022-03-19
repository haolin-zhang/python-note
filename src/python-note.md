# Python Basics

## Primitive Data Type

- Number

When integer operates with float, Python automatically convert integer into float.

```python
# "**" means power operation
var_float = 5.0
var_result = var_float ** 2
print(var_result) # 25.0
```

- String

Modulo operation on string: replace a special character in string with an assigned value.

```python
# "%" mark the space where attribute needs to be inserted into string
# "%s" means input is string
var_name = "Eric"

var_greeting = "Hello, %s." % name

# "%.6f" means input type is float and should be display in 6 digits
var_value = 5.0
var_banel = “Number is: %.6f” % var_value
```

## Collection

There are 4 built-in types of collections in Python: List, Set, Dictionary, Tuple.

- Set

```python
# define set
nameSet = {"school", "company", "government"}

# print elements in set
for element in nameSet:
    print(element)
```

- List

```python
nameList = ["Alice", "Bella", "Cynthia"]

# print index of item (if exists in list)
print(nameList.index("Alice"))

# print items in list
for item in nameList:
    print(item)
```

- Tuple

In Python, Tuple is similar to List and the only difference is Tuple is immutable.

```python
fruitTuple = ("apple", "banana", "cherry")
print(fruitTuple)
```

- Dictionary

Dictionary in Python is used to store data in "key:value" pairs. It has the same structure as JSON in JavaScript. Dictionary is changeable, but doesn't allow duplication of keys.

```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}

# print certain value based on key
print(car["brand"])

# iterate dictionary
for key in car:
    print(key, '->', car[key])
```

- List Comprehension

List comprehension is a compact syntax for creating a list from a collection (tuple, list) or string.

Syntax:

```python
newList = [expression(element) for element in oldList if condition]
```

Without list comprehension, to create a list based on a collection will be:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
    if "a" in x:
        newlist.append(x)
```

With list comprehension, to create a list from a collection will be:

```python
# create list from collection, when item's name contains letter "a"
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
```

Condition is a filter for creating new list, only accept items that fits the condition. Condition is optional and can be omitted.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits]
```

In list comprehension, new list can be created from iterable object.

```python
# use range() function to create an iterable object
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in range(10)]

# use iterable object with condition
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in range(10) if x < 5]
```

Expression is the operation on the item selected for creating the new list.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x.upper() for x in fruits]

# set all values in the new list to "hello"
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = ["hello" for x in fruits]

# use expression with condition: for item "banana", return "orange" instead.
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x if x != "banana" else "orange" for x in fruits]
```

## Logic Block

- Condition

```python
# if-else statement
var_x = 40
var_y = 20

if var_x > var_y:
    print("X is greater than Y.")
elif var_x == var_y:
    print("X equals to Y.")
else:
    print("Input error.")
```

- Loop

```python
# for loop
for f in fruits:
    print(f)

print(len(fruits))

fruits = ["apple", "banana", "orange"]
print(len(fruits))
for i in range(len(fruits)):
    print(fruits[i])

# while loop
num = 5
while num < 10:
    print(num)
    num += 1
    if num == 8:
        break
```

## Exception Handling

```python
# except: catch exception
# finally: deploy final run code
while True:
    try:
        number = int(input('Input a number \n'))
        print('Number input is: ' + str(number))
    except ValueError:
        print('Input is not a number!')
        break
    except ZeroDivisionError:
        print('Zero can not be division!')
        break
    except:
        break
    finally:
        print('Input end.')
```

## Function

```python
# declare function
def printSomething():
    print("Hello, this is the first function.")

printSomething()
```

- With Single Argument

```python
# function with argument
def function_convert(age):
    if type(age) != int:
        pass
    else:
        print(age)
    return age

now_age = function_convert(15)

# function with default value
def get_gender(gender = 'unknown'):
    if gender is 'm':
        gender = 'Male'
    elif gender is 'f':
        gender = 'Female'
    print(gender)

get_gender()
get_gender('m')
get_gender('f')
```

- Attribute Scope

In Python variable defined in function is default local type, but can be forced set to global type:

```python
x = 5

# force set x as global attribute
def scopeTest():
    global x
    print(x)
    print(x + 5)

scopeTest()
```

- With Flexible Num of Arguments

```python
def add_numbers(*args):
    total = 0
    for a in args:
        total = total + a
    print(total)

add_numbers(1,2,3,4,5,6)
add_numbers(1,2,3)
```

- With Key Word Argument

```python
# function with key word argument
# here keyWordArg is a dictionary
def printMap(**keyWordArg):
    print(type(keyWordArg))
    for arg in keyWordArg.items():
        print(arg)

printMap(x = 3, y = 5)
```

## Package & Pip & Virtual Environment

- Pip With Library Installation

Library: collections of functions saved together.

PIP is a package manager for Python. It is usually installed with Python environment. Common used commands includes:

```python
# check PIP version
pip --version

# download install Python package (module)
pip install matplotlib

# uninstall Python package
pip uninstall matplotlib

# list all installed packages
pip list
```

- Virtual Environment

In Python, different applications can use different virtual environments. The module used to create and manage virtual environments is called venv, which comes with Python installation.

```python
# create a virtual environment "demo-env"
# command will create a directory "demo-env" under current directory
python -m venv demo-env

# activate virtual environment
{.\Scripts} activate

# deactivate virtual environment
{.\Scripts} deactivate
```

Once activating the virtual environment, the line below "{.\Scripts} activate" command will has "({env-name})" as prefix.

Once deactivating the virtual environment, the "({env-name})" prefix will disappear.

```python
# verify if virtual environment is activated
pip -V
```

After activating the virtual environment, command "pip -V" will give the path of current workspace: "{env-name}\lib\site-packages\pip ({python-version})", instead of the Python installation path.

```python
# install module in virtual environment
pip intall matplotlib
```

After installation, all modules will be installed within the "{env-name}\Lib\site-packages".

- Import Module

In custom.py

```python
def print_fruit():
    print('apple')
    print('Banana')
```

In app.py

```python
import custom

# import module
custom.print_fruit()
```

## File Operation

- Write to File

```python
# file write
# "w": write in file (if file not exists, it will create a new file)
# "a": append file (to an existing file)
fw = open("~/Desktop/workspace/sample.txt", "w")
fw.write("This is a file writing example.")
fw.close()
```

- Read File

```python
# file read
# "r": read file
fr = open("~/Desktop/workspace/sample.txt", "r")

# read the whole file
text = fr.read()
print(text)

# read file line by line
for line in f:
	print(line)

fr.close()
```

- Download a photo:

```python
import random
import urllib.request

def download_web_image(url):
    name = random.randrange(1, 1000)
    full_name = str(name) + ".jpg"
    urllib.request.urlretrieve(url, full_name)

# start downloading
download_web_image("http://cms-bucket.nosdn.127.net/3fd.jpeg")
```

- Download a CSV file:

```python
from urllib import request

def download_stock_data(url):

    # get response from URL
    response = request.urlopen(url)

    # convert download data into string
    csv_data = response.read()
    csv_str = str(csv_data)
    lines = csv_str.split("\\n")

    # create a file
    file_dest = "C:/Users/John/Desktop/file/tesla_data.txt"
    csv_file = open(file_dest, "w")

    # write in file
    for line in lines:
        csv_file.write(line + "\n")

    # close file
    csv_file.close()

# start downloading
download_stock_data("https://www.apache.org/")
```

## Navigating Directory

os library is used in Python for navigating and operating directories.

```python
import os

# get current directory
print(os.getcwd())

# list contents in current directory
print(os.listdir())

# change directory
path = "~/Desktop/workspace/"
os.chdir(path)

# make a new directory
path = "~/Desktop/workspace/new-repository/"
os.mkdir(path)

# rename a directory
os.rename("/new-name", "/old-name")
```
