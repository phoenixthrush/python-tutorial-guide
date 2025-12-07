# Comments

You can use comments to explain Python code, make your code more readable, or prevent the execution of a line. Just start the line with a `#` at the beginning.

```python
# This is a comment
print("Hello, World!")
```

You can place comments at the end of a line, and Python will ignore everything after the comment. Inline comments should be separated from the statement by at least two spaces.

```python
print("Hello, World!")  # This is another comment
```

A comment does not have to be an explanation of the code. It can also be used to prevent Python from executing the code.

```python
# print("Hello, World!")
print("Hello, World!")
```

## Multiline Comments

To add a multiline comment, insert a `#` on each line.

```python
# This
# is
# a
# comment
print("Hello, World!")
```

Since Python ignores unassigned string literals, you can add a multiline string (triple quotes) to your code and put your comment inside it.

```python
"""
This
is
a
comment
"""
print("Hello, World!")
```

---

[<- Previous: Output](Output.md) | [Next: Variables ->](Variables.md) | [Table of Contents](../README.md)
