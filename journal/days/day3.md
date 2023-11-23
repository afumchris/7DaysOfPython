# Day 3 - Python Data Structures and OOP

Welcome to the third day of Python, and today we will cover some more advanced concepts:

- Data Structures
- Object Oriented Programming (OOP)

## Data Structures:

Python includes a number of data structures for storing and organizing data. The following are some of the most common ones:

### Lists:

Lists are used to store multiple items in a single variable. They can hold any type of collection of items (including other lists), and their elements can be accessed via an index.
Lists are mutable, which means they can be changed by adding, removing, or changing elements.

Example, Create a List:
```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

output
```
['apple', 'banana', 'cherry']
```

Example on how to access elements in a list:

``` python
thislist = ["apple", "banana", "cherry"]
print(thislist[0]) # OUTPUT apple
print(thislist[2]) # OUTPUT cherry
```

### Tuples:

Tuples are similar to lists, but they are immutable, which means they cannot be **changed** once created. They are frequently used to represent fixed sets of data.
Tuples can be created with or without parentheses, but they are typically used to make the code more readable.

Example, Create a Tuple:
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

output
```
('apple', 'banana', 'cherry')
```

Example on how to access elements in a Tuple:
``` python
my_tuple = (1, 2, "three", [4, 5])
print(my_tuple[0])   # OUTPUT 1
print(my_tuple[2])   # OUTPUT "three"
print(my_tuple[3][0]) # OUTPUT 4
```

### Dictionaries:

Dictionaries are yet another versatile Python data structure that stores a collection of key-value pairs. The keys must be unique and unchangeable (strings and numbers are common), and the values can be of any type.
Dictionaries can be changed by adding, removing, or changing key-value pairs.

Example:
``` python
my_dict = {"name": "Chris", "project": "letstalkmovies", "country": "Nigeria"}
print(my_dict["name"])   # OUTPUT "Chris"
print(my_dict["project"])   # OUTPUT "letstalkmovies"
print(my_dict["country"])  # OUTPUT "Nigeria"
```

### Sets:

Sets are used to store multiple items in a single variable. They are frequently used in mathematical operations such as union, intersection, and difference.
Sets are mutable, which means they can be added or removed, but the elements themselves must be immutable and sets cannot have two items with the same value.
Here's an example of how to make a set and then perform operations on it:

``` python
my_set = {1, 2, 3, 4, 5}
other_set = {3, 4, 5, 6, 7}
print(my_set.union(other_set))  # {1, 2, 3, 4, 5, 6, 7}
print(my_set.intersection(other_set)) # {3, 4, 5}
print(my_set.difference(other_set))  # {1, 2}
```

## Object Oriented Programming:











