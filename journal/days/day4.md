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


``` python
import re

# Search for a phone number in a string
text = 'My phone number is 555-7777'
match = re.search(r'\d{3}-\d{4}', text)
if match:
    print(match.group(0))

# Extract email addresses from a string
text = 'My email is example@devops.com, but I also use other@cloud.com'
matches = re.findall(r'\S+@\S+', text)
print(matches)
```

Output:

``` bash
555-7777
['example@devops.com,', 'other@cloud.com']
```

Here's a breakdown:

  - Importing the `re` Module: `import re`, This line imports the `re` module, which provides support for regular expressions in Python.
  - Searching for a Phone Number:
    
     ```python
     text = 'My phone number is 555-7777'
     match = re.search(r'\d{3}-\d{4}', text)
     if match:
     print(match.group(0))
     ```
       - `text = 'My phone number is 555-7777'`, Initializes a string variable text containing a sentence with a phone number.
       - `re.search(r'\d{3}-\d{4}', text)`, Uses `re.search` to look for a pattern in the text. The pattern `\d{3}-\d{4}` matches three digits, a hyphen, and four more digits (a common format for phone numbers). The result is stored in the `match` variable.
       - `if match: print(match.group(0))`, Checks if a match was found. If yes, it prints the matched phone number using `match.group(0)`.
   
  - Extracting Email Addresses:

    ```python
    text = 'My email is example@devops.com, but I also use other@cloud.com'
    matches = re.findall(r'\S+@\S+', text)
    print(matches)
    ```
      - `text = 'My email is example@devops.com, but I also use other@cloud.com'`, Initializes another string variable `text` containing a sentence with email addresses.
      - `re.findall(r'\S+@\S+', text)`, Uses `re.findall` to find all occurrences of email addresses in the text. The pattern `\S+@\S+` matches one or more non-whitespace characters, followed by an '@' symbol, and then one or more non-whitespace characters again.
      - `print(matches)`, Prints all the email addresses found in the text.
   
  - Output:
    
    ```python
    555-7777
    ['example@devops.com,', 'other@cloud.com']
    ```
    
The output demonstrates that the code successfully found and printed a phone number and a list of email addresses based on the specified patterns in the given strings. The regular expressions used in this code are powerful tools for pattern matching within text data.

## Datetime library:

As the name suggests, Python's `datetime` module allows you to work with dates and times in your code. It includes functions for formatting and manipulating date and time data, as well as classes for representing dates, times, and time intervals.
The datetime module, for example, can be used to get the current date and time, calculate the difference between two dates, or convert between different date and time formats.

``` python
from datetime import datetime, timedelta

# Get the current date and time
now = datetime.now()
print(now) # Output: 2023-02-17 11:33:27.257712

# Create a datetime object for a specific date and time
date = datetime(2023, 2, 1, 12, 0)
print(date) # Output: 2023-02-01 12:00:00

# Calculate the difference between two dates
delta = now - date
print(delta) # Output: 15 days, 23:33:27.257712
```

Output:

``` bash
2023-02-17 11:33:27.257712
2023-02-01 12:00:00
15 days, 23:33:27.257712
```

The provided Python code demonstrates the usage of the datetime module for working with dates and times. Below is the breakdown:

  - Importing `datetime` and `timedelta` Classes: `from datetime import datetime, timedelta`, This line imports the `datetime` class and the `timedelta` class from the `datetime module`. datetime is used for representing dates and times, and `timedelta` is used for representing time intervals.
  - Getting the Current Date and Time:
    ```python
    now = datetime.now()
    print(now)
    ```
      - `datetime.now()`: This function returns a `datetime` object representing the current date and time.
      - `print(now)`: It prints the current date and time. The output format includes the year, month, day, hour, minute, second, and microsecond.

  - Creating a Datetime Object for a Specific Date and Time:
    ```python
    date = datetime(2023, 2, 1, 12, 0)
    print(date)
    ```
    - `datetime(2023, 2, 1, 12, 0)`: This line creates a `datetime` object representing the date February 1, 2023, at 12:00 PM.
    - `print(date)`: It prints the specified date and time.
   
    - 








