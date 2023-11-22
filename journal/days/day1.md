# Day 1 - Introduction to Python

In the late 1980s, Python was conceived by Guido van Rossum as a high-level, interpreted, and dynamic programming language. Its extensive usage spans various domains such as web development, devops, data analysis, alongside applications in artificial intelligence and machine learning

## Installation and Setting up the Environment:

Python is available for download and installation on a variety of platforms, including Windows, Mac, and Linux. Python can be downloaded from [the official website](https://www.python.org/.).

Following the installation of Python, you can configure your environment with an Integrated Development Environment (IDE) such as [PyCharm](https://www.jetbrains.com/pycharm/), [Visual Studio Code](https://code.visualstudio.com/), or IDLE (the default IDE that comes with Python).
I personally use Visual Studio Code.

You can also use cloud environment, where you will not have to configure and install python locally, like [Replit](https://replit.com/).

## Basic Data Types:

Python provides several built-in data types designed for storing and manipulating data, with the following being the most common ones:

  - Integers (`int`): Whole numbers without decimal points. Example: `5`, `-10`, `1000`
  - Floats (`float`): Numbers that can have decimal points for more precision. Example: `3.14`, `-0.5`, `2.0`
  - Strings (`str`): Sequences of characters, enclosed in single (' ') or double (" ") quotes. Example: `"Hello, Python!"`, `'123'`
  - Booleans (`bool`): Represents truth values, either True or False. Example: `True`, `False`
  - Lists (`list`): Ordered collections that can contain elements of different data types. Example: `[1, 2, 3]`, `['apple', 'banana', 'orange']`
  - Tuples (`tuple`): Similar to lists but immutable (cannot be changed after creation). Example: `(1, 2, 3)`, `('red', 'green', 'blue')`
  - Dictionaries (`dict`): Key-value pairs, allowing you to store and retrieve data using keys. Example: `{'name': 'John', 'age': 25}`, `{'city': 'New York', 'population': 8_398_748}`
  - Sets (`set`): Unordered collections of unique elements. Example: `{1, 2, 3}`, `{'apple', 'orange', 'banana'}`

## Operations and Expressions:

With the above data types, you can perform a variety of operations in Python, including arithmetic, comparison, and logical operations.
Expressions can also be used to manipulate data, such as combining multiple values into a new value.

Arithmetic Operations:

Addition (+): Combining numbers, like 3 + 5.
Subtraction (-): Finding the difference, such as 8 - 2.
Multiplication (*): Repeated addition, like 4 * 3.
Division (/): Sharing, for example, 10 / 2.
Exponentiation ():** Raising a number to a power, like 2 ** 3 (which means 2 raised to the power of 3).

Comparison Operators:

Equal (==): Checks if two values are equal.
Not Equal (!=): Checks if two values are not equal.
Greater Than (>): Tests if one value is greater than another.
Less Than (<): Tests if one value is less than another.
Greater Than or Equal To (>=): Checks if one value is greater than or equal to another.
Less Than or Equal To (<=): Checks if one value is less than or equal to another.

Logical Operators:

and: Returns True if both conditions are true.
or: Returns True if at least one condition is true.
not: Returns True if the condition after it is false, and vice versa.

Expressions:

These are combinations of values, variables, and operators that can be evaluated to produce a result. For example, 2×(3+4). 2×(3+4) is an expression.

## Variables:

Variables are used to store and manage data. A variable is essentially a name assigned to a memory location that holds a value. When you create a variable, you are allocating space in memory to store data, and you can later reference that data using the variable name. Python is dynamically typed, meaning you don't need to explicitly declare the data type of a variable; Python infers it based on the assigned value.

Here's a basic example of variable usage in Python:
```
# Variable assignment
age = 20
name = "Chris"
height = 1.95
```

In this example, `age`, `name`, and `height` are variables storing an integer, a string, and a float, respectively. Python allows you to reassign values to variables during the program execution, making it flexible and dynamic.

Variable names are case-sensitive and may consist of letters, numbers, or underscores ( _ ). However, they must not commence with a numeral. Additionally, among the frequently employed data types involving numbers, strings are prominent. A string is a series of one or more characters and is typically defined using single quotation marks. Nonetheless, double quotation marks can also be employed, as illustrated below in Python:
```
a = 'My name is Chris'
b = "This is also a string"
```
You can add strings to other strings — an operation known as "concatenation" — with the same + operator that adds two numbers:

``` python
x = 'My name is' + ' ' + 'Chris'
print(x) # outputs: My name is Chris
```

## Printing to the console:

The print function in Python is one of more than 60 built-in functions. It outputs text to the screen.
Let's see an example of the most famous "Hello World!":

``` python
print('Hello World!')
```

The print argument is a string, which is one of Python's basic data types for storing and managing text. Print outputs a newline character at the end of the line by default, so subsequent calls to print will begin on the next line.

## Resources:

- [Learn Python - Full course by freeCodeCamp](https://youtu.be/rfscVS0vtbw)
- [Python tutorial for beginners by Nana](https://youtu.be/t8pPdKYpowI)
- [Python Crash Course book](https://amzn.to/40NfY45)



