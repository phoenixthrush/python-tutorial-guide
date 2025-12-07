# Data Types

Python variables can store different types of data, each suited for specific tasks.

Common types include text (`str`), numbers (`int`, `float`, and `complex`), and collections such as lists, tuples, ranges, dictionaries, and sets.

There are also booleans (`bool`), binary data (`bytes`, `bytearray`, and `memoryview`), and more. The NoneType represents a lack of value.

Selecting the appropriate data type affects how the data can be used and manipulated in your programs.

- Text Type: `str`
- Numeric Types: `int`, `float`, `complex`
- Sequence Types: `list`, `tuple`, `range`
- Mapping Type: `dict`
- Set Types: `set`, `frozenset`
- Boolean Type: `bool`
- Binary Types: `bytes`, `bytearray`, `memoryview`
- None Type: `NoneType`

```python
# Text Type
name = "Alice"  # str: a string of text
greeting = 'Hello'  # str: single-quoted string also works

# Numeric Types
age = 25  # int: whole number
height = 1.75  # float: number with decimal point
z = 2 + 3j  # complex: number with real and imaginary parts

# Sequence Types
fruits = ["apple", "banana", "cherry"]  # list: ordered, mutable collection
coordinates = (10, 20)  # tuple: ordered, immutable collection
numbers_range = range(5)  # range: sequence of numbers

# Mapping Type
person = {"name": "Alice", "age": 25}  # dict: key-value pairs

# Set Types
unique_numbers = {1, 2, 3}  # set: unordered collection of unique items
frozen_numbers = frozenset([1, 2, 3])  # frozenset: immutable set

# Boolean Type
is_sunny = True  # bool: True or False
is_raining = False                      

# Binary Types
data_bytes = b"Hello"  # bytes: immutable sequence of bytes
data_bytearray = bytearray([72,101,108,108,111])  # bytearray: mutable bytes
data_memoryview = memoryview(b"Hello")  # memoryview: view of another binary object

# None Type
result = None  # NoneType: represents no value
```

Each of these data types will be examined in a dedicated chapter.

---

[<- Previous: Variables](Variables.md) | [Next: Numbers ->](Numbers.md) | [Table of Contents](../README.md)
