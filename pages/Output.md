# Print Stuff

## Output Text

You can use the print() function to output text to your terminal:

```python
print("Hello World!")
```

Want to print line by line? Just call print() multiple times:

```python
print("Hello World!")
print("This is Python.")
print("I like cats!")
```

Notice those quotes around the text? Those are called strings, and Python needs the quotes to know it’s text. Don’t worry, you’ll see why later when we talk about variables. For now, just remember: strings = quotes, either double `"` or single `'`:

```python
print("This will work!")
print('This will also work!')
```

Sometimes, it's useful to print text without a new line. To do so, use the `end` parameter inside the print function. Python sets the end parameter to `\n` by default. You can overwrite this behavior to fit your needs.

For example, you can use a space character to separate the lines instead of a new line.

```python
print("Hello World!", end=" ")
print("I will print on the same line.")
```

There are other escape sequences that use a backslash at the beginning, which will be taught in another chapter. The most important ones are:

```python
# Newline (line break)
print("Hello", end="\n")
print("World!")

#  Horizontal Tab
print("Name:\tApple")
print("Price:\t$1")
```

## Output Numbers

You can also use the `print()` function to display numbers. However, unlike text, numbers are not placed inside quotes.

```python
print(1)
print(2)
print(3)
```

You can also perform math operations using arithmetic operators within the print() function.

```python
# Addition: adds two numbers together
print(3 + 2)  # 5 because 3 + 2 = 5

# Subtraction: subtracts the second number from the first
print(3 - 2)  # 1 because 3 - 2 = 1

# Multiplication: multiplies two numbers
print(3 * 2)  # 6 because 3 times 2 = 6

# Division (float): divides the first number by the second, result is always a float
print(3 / 2)  # 1.5 because 3 divided by 2 = 1.5

# Floor division: divides the first number by the second and rounds down to nearest whole number
print(3 // 2)  # 1 because 3 divided by 2 is 1.5, rounded down = 1

# Modulus (remainder): gives the remainder of the division
print(3 % 2)  # 1 because 3 divided by 2 leaves a remainder of 1

# Exponentiation: raises the first number to the power of the second
print(3 ** 2)  # 9 because 3 squared (3 * 3) = 9
```

If you are German, it's important to know that Python uses English formats, so floating-point numbers are written using a dot and not a comma. You will understand this when reading about assigning variables.

```python
print(3 * 1.5)
```

You can combine text and numbers in a single output by separating them with commas:

```python
print("I am", 20, "years old.")
```

Python introduced f-strings, the modern and preferred method for formatting strings. Before Python 3.6, older, less readable methods were used.

```python
# Using % formatting
print("My name is %s and I am %d years old." % (name, age))

# Using str.format()
print("My name is {} and I am {} years old.".format(name, age))
```

Use f-strings to keep your code clean and easy to read. To use them, simply add an `f` character at the beginning of the string and wrap any variables in curly braces `{}`.

```python
name = "Alice"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

---

[Next: Comments ->](Comments.md) | [Table of Contents](../README.md)
