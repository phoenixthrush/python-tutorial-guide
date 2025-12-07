# Numbers

In Python, there are three numeric types:

- int
- float
- complex

Numeric variables are created when a value is assigned to them.

```python
x = 1  # int
y = 4.5  # float
z = 1j  # complex

print(type(x))  # <class 'int'>
print(type(y))  # <class 'float'>
print(type(z))  # <class 'complex'>
```

## Int

An integer is a whole number, either positive or negative, with no decimal places and of unlimited length.

```python
x = 5
y = 123456789
z = -42

print(type(x))  # <class 'int'>
print(type(y))  # <class 'int'>
print(type(z))  # <class 'int'>
```

## Float

A float, also known as a "floating-point number," is a positive or negative number containing one or more decimal places.

```python
x = 1.25
y = 5.0
z = -50.25

print(type(x))  # <class 'float'>
print(type(y))  # <class 'float'>
print(type(z))  # <class 'float'>
```

Float can also be scientific numbers with an "e" to indicate the power of 10.

```python
x = 50e3
y = 25E5
z = -40e250
```

## Complex

Complex numbers are written with an "j" to represent the imaginary part.

```python
x = 3 + 5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```

## Type Conversion

The `int()`, `float()`, and `complex()` methods allow you to convert from one type to another.

```python
x = 1  # int
y = 2.5  # float
z = 1j  # complex

# convert from int to float
a = float(x)

# convert from float to int
b = int(y)

# convert from int to complex
c = complex(x)

print(a)  # 1.0
print(b)  # 2
print(c)  # (1+0j)

print(type(a))  # <class 'float'>
print(type(b))  # <class 'int'>
print(type(c))  # <class 'complex'>
```

## Random Number

Python includes a built-in module called random that provides several ways to generate random values.

```python
import random

random.random()                 # float between 0 and 1
random.randint(1, 10)           # random integer from 1 to 10 (inclusive)
random.randrange(1, 10)         # random number from range 1–9
random.randrange(0, 20, 2)      # random even number between 0 and 18
random.uniform(1.5, 5.5)        # random float between 1.5 and 5.5

random.choice([1, 2, 3, 4])     # random element from list
random.choice("hello")          # random character from string
random.choices([1, 2, 3], k=5)  # list of 5 random elements (with repeats)
random.sample([1, 2, 3, 4], 2)  # list of 2 unique elements (no repeats)

lst = [1, 2, 3, 4, 5]
random.shuffle(lst)             # shuffles list in place

random.seed(42)                 # sets seed for reproducible results
random.getrandbits(8)           # random integer using 8 random bits (0–255)
```

---

[<- Previous: Data Types](Data-Types.md) | [Next: Casting ->](Casting.md) | [Table of Contents](../README.md)
