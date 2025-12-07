# Variables

A variable is a container for storing data values.

Rules for Python variables:

- A variable name must begin with a letter or an underscore.
- A variable name cannot begin with a number.
- A variable name can only contain alphanumeric characters and underscores (a-Z, 0-9, and _).
- Variable names are case-sensitive. This means that "age," "Age," and "AGE" are three different variables.
- A variable name cannot be one of the Python keywords.

Variable names consisting of more than one word can be difficult to read.

There are several techniques you can use to improve readability, but Python recommends Snake Case. This means each word is separated by an underscore character.

```python
this_is_a_var = "John"
```

To create a variable, you must first assign a value to it.

```python
x = 3
y = "Cats"

print(x)
print(y)
```

Variables do not need to be declared as a specific type, and they can change type after being set. We will discuss data types in a later chapter. For now, it is sufficient to know that Python allows this.

```python
x = 50  # x is of type int
x = "Cats"  # x is now of type str

print(x)
```

You can specify the data type of a variable with casting.

```python
x = str(3)  # x will be '3'
y = int(3)  # y will be 3
z = float(3)  # z will be 3.0
```

Use the `type()` function to determine the data type of a variable.

```python
a = "John"
b = 5
c = str(3)
d = int(3)
e = float(3)

print(type(a))  # <class 'str'>
print(type(b))  # <class 'int'>
print(type(c))  # <class 'str'>
print(type(d))  # <class 'int'>
print(type(e))  # <class 'float'>
```

You can declare string variables using either single or double quotes. Choose the option that makes your string easier to read and avoids unnecessary escaping of quotes.

```python
x = "Cat"
# is the same as
x = 'Cat'
```

Note that variable names are case-sensitive.

```python
a = 4
A = "Sally"  # A will not overwrite a
```

With Python, you can assign values to multiple variables in one line.

```python
x, y, z = "Orange", "Banana", "Cherry"

print(x)  # Orange
print(y)  # Banana
print(z)  # Cherry
```

You can also assign the same value to multiple variables on one line.

```python
x = y = z = "Orange"

print(x)  # Orange
print(y)  # Orange
print(z)  # Orange
```

If you have a collection of values in a list or tuple, for example, , Python allows you to extract those values into variables. This process is called unpacking. You will learn what lists and tuples are in the chapter about data types.

```python
fruits = ["Apple", "Banana", "Cherry"]
x, y, z = fruits

print(x)  # Apple
print(y)  # Banana
print(z)  # Cherry
```

---

[<- Previous: Comments](Comments.md) | [Next: Data Types ->](Data-Types.md) | [Table of Contents](../README.md)
