# Day 4 - Python: Debugging, testing and Regular expression

Welcome to Day 4 of Python!
Today we will learn about:

- Debugging and testing
- Regular expressions
- Datetime library

Let's start!

## Debugging and testing

Debugging is the process of finding and correcting errors or bugs in code. Python includes a debugger called `pdb` that allows you to step through your code and inspect variables as you go. You can use `pdb` to help you figure out where your code is going wrong and how to fix it.

``` python
import pdb

def add_numbers(x, y):
    result = x + y
    pdb.set_trace() # Start the debugger at this point in the code
    return result

result = add_numbers(2, 3)
print(result)
```

The provided Python code demonstrates the use of the `pdb` debugger. Here's a breakdown:

  - Importing the `pdb` Module: `import pdb`, This line imports the `pdb` module, which provides the Python debugger functionalities.
  - Defining the `add_numbers` Function: `def add_numbers(x, y)`:, This function takes two parameters, `x` and `y`, adds them, sets a breakpoint using `pdb.set_trace()`, and then returns the result.
  - Using `pdb.set_trace()`: `pdb.set_trace()`, This line sets a breakpoint in the code. When the program execution reaches this point, it will pause, and you can interactively debug and inspect variables using the `pdb` commands.
  - Calling the `add_numbers` Function: result = `add_numbers(2, 3)`, This line calls the `add_numbers` function with the arguments 2 and 3, triggering the debugger.
  - Printing the Result: `print(result)`, This line prints the result obtained from the `add_numbers` function.





