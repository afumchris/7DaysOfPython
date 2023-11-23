# Day 2 - Python Loops, functions, modules and libraries

Welcome to the second day of Python, and today we will cover some more concepts:
- Loops
- Functions
- Modules and libraries
- File I/O
- Exception Handling

## Loops (for/while):

Loops are used to repeatedly run a block of code.

### for loop

A `for loop` is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

Example, print each fruit in a fruit list:
```python
fruits = ["grapes", "cherry", "apple"]
for x in fruits:
  print(x)
```

output
```
grapes
cherry
apple
```

### while loop

The `while loop` is used to execute a block of code repeatedly as long as a condition is True.

Example, print i as long as i is less than 6:
```python
i = 1
while i < 6:
  print(i)
  i += 1
```

output
```
1
2
3
4
5
```

## Functions
A function is a block of code which only runs when it is called, you can pass data, known as parameters, into a function, a function can return data as a result. Using the `def` keyword in Python, you can define a function. In your programme, functions can be used to encapsulate complex logic and can be called several times. Functions can also be used to simplify code and make it easier to read.

Example:
```python
def my_function():
  print("Hello from a function")

my_function()
```

output
```
Hello from a function
```

Here is an illustration of a function that adds two numbers:

``` python
# function has two arguments num1 and num2
def add_numbers(num1, num2):
    sum = num1 + num2
    print('The sum is: ',sum)
```

``` python
# calling the function with arguments to add 5 and 2
add_numbers(5, 2)

# Output: The sum is: 7
```

## Understanding Modules and Importing Libraries:

Modules: Files containing Python code, which can define functions, variables, and classes. You can use them in other programs.
Libraries: Collections of modules. They provide pre-written code for common tasks.
Additional libraries can be installed using package managers like pip.
You must import a module or library using the import statement in order to use it in your programme.

Example:
```python
import math
result = math.sqrt(25)
```

output
```
5.0
```

## File I/O

File I/O is used to read and write data to and from files on disk.
The built-in Python function open() can be used to open a file, after which you can read from and write to it using methods like read() and write().
To save system resources, you should always close the file after you are done with it.

Example of reading from a file:
```python
f = open("examplefile.txt", "r")
print(f.read())
f.close()
```

Example of writing to a file:
```python
f = open("example.txt", "a")
f.write("Now the file has more content!")
f.close()
```

## Exception Handling:

Exceptions are runtime errors that happen when your programme runs into unexpected circumstances, such dividing by zero or attempting to access a list element that doesn't exist.
Using a try/except block, you can manage exceptions in Python. The try block's code is run, and if an exception arises, the except block's code is run to handle the exception.

``` python
try:
  f = open("example.txt")
  try:
    f.write("Python is great")
  except:
    print("Something went wrong when writing to the file")
```







