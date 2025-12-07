# Operators

## Arithmetic Operators

You already know the arithmetic operators from the chapter before in the [Output](pages/Output.md) chapter.

| Operator | Name           | Example  |
|----------|----------------|----------|
| +        | Addition       | x + y    |
| -        | Subtraction    | x - y    |
| *        | Multiplication | x * y    |
| /        | Division       | x / y    |
| %        | Modulus        | x % y    |
| **       | Exponentiation | x ** y   |
| //       | Floor division | x // y   |

## Assignment Operators

Assignment operators are used to store values in variables and can also modify them based on their current value.

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| =        | x = 3   | x = 3      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| //=      | x //= 3 | x = x // 3 |
| **=      | x **= 3 | x = x ** 3 |
| &=       | x &= 3  | x = x & 3  |
| \|=      | x \|= 3 | x = x \| 3 |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |
| <<=      | x <<= 3 | x = x << 3 |
| :=       | print(x := 3) | x = 3; print(x) |

## The Walrus Operator (:=)

The Walrus Operator (:=)

```python
numbers = [1, 2, 3, 4, 5]

# Traditional way
count = len(numbers)
if count > 3:
    print(f"List has {count} elements")

# Using walrus operator
if (count := len(numbers)) > 3:
    print(f"List has {count} elements")
```

This way, you don’t need a separate line to assign and then check the value.

## Comparison Operators

---

[<- Previous: Booleans](Booleans.md) | [Next: Lists ->](Lists.md) | [Table of Contents](../README.md)
