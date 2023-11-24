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

In addition to debugging, testing is crucial for ensuring that your code behaves as expected. The provided code demonstrates a simple example of testing using the `unittest` module:

``` python
import unittest

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True

class TestIsPrime(unittest.TestCase):
    def test_is_prime(self):
        self.assertTrue(is_prime(2))
        self.assertTrue(is_prime(3))
        self.assertTrue(is_prime(5))
        self.assertFalse(is_prime(4))

if __name__ == '__main__':
    unittest.main()

```

Output:

``` bash
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```

  - Defining the `is_prime` Function: `def is_prime(n):`, This function checks if a given number `n` is prime. It returns `True` if `n` is prime and `False` otherwise.
  - Creating a Test Class: `class TestIsPrime(unittest.TestCase):`, This class inherits from `unittest.TestCase` and defines test cases for the `is_prime` function.
  - Writing Test Cases:
     - `self.assertTrue(is_prime(2))`, This line asserts that the function correctly identifies 2 as a prime number.
     - `self.assertTrue(is_prime(3))`, This line asserts that the function correctly identifies 3 as a prime number.
     - `self.assertTrue(is_prime(5))`, This line asserts that the function correctly identifies 5 as a prime number.
     - `self.assertFalse(is_prime(4))`, This line asserts that the function correctly identifies 4 as a non-prime number.
  - Running the Tests: `if __name__ == '__main__': unittest.main()`, This block runs the tests when the script is executed directly.
  - Test Output: The output (`OK`) indicates that all the test cases passed successfully.


Additional Note:
Testing helps ensure that your code works correctly and allows you to catch and fix issues early in the development process.

## Regular expressions:

Regular expressions (regex or regexp) provide a powerful way to search, match, and manipulate text patterns. The provided Python code demonstrates the use of regular expressions using the re module.





