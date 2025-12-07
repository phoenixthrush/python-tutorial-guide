# Booleans

Booleans represent truth values in Python. A Boolean can be either `True` or `False`.

In programming, we often check whether something is true or not.
A Boolean value is the result of evaluating an expression.

```python
print(10 > 3)  # True
print(5 == 2)  # False
```

`If` statements use Boolean values to determine which code to run.

```python
a = 200
b = 30

if b > a:
    print("b is greater than a")
else:
    print("b is not greater than a")
```

The `bool()` function converts any value into `True` or `False`.

Python treats most non-empty or non-zero values as True:

```python
print(bool("Hello"))  # True
print(bool(15))  # True
print(bool(["apple", "banana"]))  # True
```

Only a few values evaluate to False:

- `False`
- `None`
- `0`
- `""` (empty string)
- `[]` (empty list)
- `{}` (empty dict)
- `()` (empty tuple)
- Objects with a `__len__()` method that returns 0

```python
bool(False)
bool(0)
bool("")
bool([])
bool({})
```

A function can return True or False:

```python
def is_valid():
    return True

print(is_valid())  # True
```

You can use the return value in conditions:

```python
def check():
    return True

if check():
    print("YES!")  # this will run
else:
    print("NO!")
```

Python has many built-in functions that return Booleans.
For example, isinstance() checks a value’s type:

```python
x = 200
print(isinstance(x, int))  # True
```

---

[<- Previous: Strings](Strings.md) | [Next: Operators ->](Operators.md) | [Table of Contents](../README.md)
