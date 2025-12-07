# Strings

In Python, a string is a sequence of characters that are enclosed by either single or double quotation marks.

```python
'hello'
"hello"
```

Both forms create the same type of string.
You can display a string by using the `print()` function.

You can place quotes inside a string as long as they do not match the ones used to enclose the string.

```python
print("It's alright")
print("He is called 'Findus'")
print('He is called "Findus"')
```

In Python, you can write strings across multiple lines by enclosing them in either three single or double quotes.

```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""

print(a)
```

```python
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''

print(a)
```

The line breaks appear in the output exactly as written in the code.

```plain
Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.
```

In Python, a string behaves like an array of characters.
There is no separate character type; a single character is simply a string of length one.

You can access individual characters by using square brackets.

```python
a = "Hello, World!"
print(a[1])  # e
```

At first, you might expect `a[1]` to return `H`, but it returns `e` instead.
This is because Python starts counting at 0.

That means:

- The first character is at position 0
- The second character is at position 1
- The third character is at position 2
- ... and so on

This zero-based indexing applies to strings, lists, and many other Python structures.

Since strings are sequences, you can loop through them one character at a time.

```python
for letter in "banana":
    print(letter)

# b
# a
# n
# a
# n
# a
```

Use the `len()` function to find out how many characters a string contains.

```python
length = len("Hello")
print(length)  # 5
```

Use the `in` keyword to check if a substring appears in a string.

```python
cats = "I love cats!"

print("love" in cats)  # True
print("dogs" not in cats)  # True

# or

if "love" in cats:
    print(True)  # True

if "dogs" not in cats:
    print(True)  # True
```

The `for` loops and `if` statements are taught in another chapter. Remember that a string behaves like an array of characters.

## Slicing

Use the slice syntax to return a range of characters.

To return a part of the string, specify the start index and the end index separated by a colon.

```python
x = "Hello, World!"
print(x[2:5])  # llo
```

If you leave out the start index, the range will start with the first character. Get the characters from the beginning to index 5 (not including index 5).

```python
x = "Hello, World!"
print(x[:5])  # Hello
```

Leaving out the end index will extend the range to the end. Get the characters from position two all the way to the end.

```python
x = "Hello, World!"
print(x[7:])  # World!
```

In Python, negative indexes can be used to access characters starting from the end of a string.
The last character has an index of -1, the second-to-last has an index of -2, and so on.

```python
x = "Hello, World!"
print(x[-5:-2])  # orl
```

This slice starts at the character `o` (which is at position -5) and goes up to but not including the character `d` (position -2).

## Modify Strings

The `upper()` method returns a string in uppercase.

```python
x = "Hello, World!"
print(x.upper())  # HELLO, WORLD!
```

The `lower()` method returns a string in lowercase.

```python
x = "HELLO, WORLD!"
print(x.lower())  # hello, world!
```

Whitespace refers to the space before and/or after the text itself. Often, you will want to remove this space.

```python
x = " Hello, World! "
print(x.strip()) #  Hello, World!
```

The `replace()` method replaces one string with another.

```python
x = "Hello, World!"
print(x.replace("H", "J"))  # Jello, World!
```

The `split()` method returns a list in which the text between the specified separator becomes the list items. It splits the string into substrings if it finds instances of the separator.

```python
x = "Hello, World!"
print(x.split(",")) #  ['Hello', ' World!']
```

## String Concatenation

You can use the + operator to concatenate, or combine, two strings.

```python
x = "Hello"
y = "World"
z = x + y

print(z)  # HelloWorld
```

Add a space between them by adding a " ":

```python
x = "Hello"
y = "World"
z = x + " " + y

print(z)  # Hello World
```

## f-strings

The f-string was introduced in Python 3.6 and has become the preferred method for formatting strings.

To specify an f-string, put an `f` in front of the string literal and add curly brackets as placeholders for variables and other operations.

Placeholders can contain variables, operations, functions, and modifiers that format values.

```python
age = 20
fish = f"My name is Findus, I am {age}"

print(fish)  # My name is Findus, I am 20
```

Placeholders can include modifiers to format values.
To do so, add a colon followed by a legal formatting type. For example, .2f means a fixed-point number with two decimals.

```python
price = 50
fish = f"The fish price is {price:.2f} dollars"

print(fish)  # The fish price is 50.00 dollars
```

Placeholders can also contain Python code, such as mathematical operations.

```python
fish = f"The fish price is {2 * 25} dollars"
print(fish)  # The fish price is 50 dollars
```

## Escape Characters

Use an escape character to insert characters that are illegal in a string.

An escape character is a backslash `\` followed by the character you want to insert.

For example, a double quote inside a string surrounded by double quotes is an illegal character.

```python
fish = "The cat said, \"I caught a fish today!\""
print(fish)  # The cat said, "I caught a fish today!"
```

## Common Escape Characters in Python

\' — Single Quote
Allows you to put a ' inside single-quoted strings.

```python
print('It\'s a cat!')  # It's a cat!
```

\\ — Backslash
Shows an actual backslash instead of starting an escape sequence.

```python
print("This is a backslash: \\")  # This is a backslash: \
```

\n — New Line
Moves the following text to a new line.

```python
print("Cats are cute.\nCats are fluffy.")

# Cats are cute.
# Cats are fluffy.
```

\r — Carriage Return
Moves the cursor to the start of the line and overwrites text.

```python
print("Cats are great!\rFish")  # Fish are great!
```

\t — Tab
Inserts a horizontal tab (indent).

```python
print("Cat:\tFish")  # Cat:    Fish
```

\b — Backspace
Deletes the previous character.

```python
print("Helloo\b!")  # Hello!
```

\ooo — Octal Value
Represents a character using octal numbers.

```python
print("\141")  # 'a'
```

\xhh — Hex Value
Represents a character using hexadecimal numbers.

```python
print("\x61")  # 'a'
```

These are the most important string methods, but there are many more. Feel free to look them up!

---

[<- Previous: Casting](Casting.md) | [Next: Booleans ->](Booleans.md) | [Table of Contents](../README.md)
