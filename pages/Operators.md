# Operators

## Arithmetic Operators

You already know the arithmetic operators from the chapter before in the [Output](Output.md) chapter.

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

| Operator | Name                       | Example  |
|----------|----------------------------|----------|
| ==       | Equal                      | x == y   |
| !=       | Not equal                  | x != y   |
| >        | Greater than               | x > y    |
| <        | Less than                  | x < y    |
| >=       | Greater than or equal to   | x >= y   |
| <=       | Less than or equal to      | x <= y   |

```python
x = 5
y = 3

print(x == y)  # False, because 5 is not equal to 3
print(x != y)  # True, because 5 is not equal to 3
print(x > y)   # True, because 5 is greater than 3
print(x < y)   # False, because 5 is not less than 3
print(x >= y)  # True, because 5 is greater than or equal to 3
print(x <= y)  # False, because 5 is not less than or equal to 3
```

Python allows you to chain comparison operators:

```python
x = 5

print(1 < x < 10)  # True
print(1 < x and x < 10)  # True
```

## Logical Operators

| Operator | Description                                                | Example               |
| -------- | ---------------------------------------------------------- | --------------------- |
| `and`    | Returns `True` if **both** statements are true             | x < 5 and x < 10      |
| `or`     | Returns `True` if **at least one** statement is true       | x < 5 or x < 4        |
| `not`    | Reverses the result, returns `False` if the result is true | not(x < 5 and x < 10) |

Test to see if a number is greater than 0 and less than 10.

```python
x = 5
print(x > 0 and x < 10)  # True
```

Test to see if a number is less than 5 or greater than 10.

```python
x = 5
print(x < 5 or x > 10)  # False
```

Reverse the result with `not`.

```python
x = 5
print(not(x > 3 and x < 10))  # False
```

## Identity Operators

Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:

| Operator | Description                                                          | Example      |
| -------- | -------------------------------------------------------------------- | ------------ |
| `is`     | Returns `True` if both variables **refer to the same object**        | `x is y`     |
| `is not` | Returns `True` if both variables **do not refer to the same object** | `x is not y` |

The is operator returns `True` if both variables refer to the same object.

```python
x = ["Cat", "Dog"]
y = ["Cat", "Dog"]
z = x

print(x is z)      # True, z points to the same object as x
print(x is y)      # False, x and y have the same content but are different objects
print(x is not y)  # True, x and y are not the same object
print(x == y)      # True, x and y have the same content/values
```

Remember, use `is` to check if two variables refer to the same object and `==` to check if their values are equal.

## Membership Operators

| Operator   | Description                                                        | Example        |
|------------|--------------------------------------------------------------------|----------------|
| `in`       | Returns True if a sequence with the specified value is present     | `x in y`       |
| `not in`   | Returns True if a sequence with the specified value is not present | `x not in y`   |

```python
# Check if "banana" is present in the list
fruits = ["apple", "banana", "cherry"]
print("banana" in fruits)  # True, because "banana" is in the list

# Check if "pineapple" is NOT present in the list
fruits = ["apple", "banana", "cherry"]
print("pineapple" not in fruits)  # True, because "pineapple" is not in the list

# Membership operators with strings
text = "Hello World"
print("H" in text)  # True, uppercase "H" is present
print("hello" in text)  # False, lowercase "hello" is not present (case-sensitive)
print("z" not in text)  # True, "z" is not present in the string
```

## Bitwise Operators

| Operator | Name                 | Description                                                                              | Example    |
|----------|----------------------|------------------------------------------------------------------------------------------|------------|
| &        | AND                  | Sets each bit to 1 if **both bits are 1**                                                | x & y      |
| |        | OR                   | Sets each bit to 1 if **one of two bits is 1**                                           | x \| y     |
| ^        | XOR                  | Sets each bit to 1 if **only one of two bits is 1**                                      | x ^ y      |
| ~        | NOT                  | Inverts all the bits                                                                     | ~x         |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right; leftmost bits fall off                    | x << 2     |
| >>       | Signed right shift   | Shift right by pushing copies of the leftmost bit from the left; rightmost bits fall off | x >> 2     |

### Bitwise AND `&`

The & operator compares each bit and set it to 1 if both are 1, otherwise it is set to 0:

```python
print(6 & 3)
```

The binary representation of 6 is 0110
The binary representation of 3 is 0011

### Bitwise OR `|`

Then the & operator compares the bits and returns 0010, which is 2 in decimal.

The | operator compares each bit and set it to 1 if one or both is 1, otherwise it is set to 0:

```python
print(6 | 3)
```

The binary representation of 6 is 0110
The binary representation of 3 is 0011

Then the | operator compares the bits and returns 0111, which is 7 in decimal.

The ^ operator compares each bit and set it to 1 if only one is 1, otherwise (if both are 1 or both are 0) it is set to 0:

### Bitwise XOR `^`

```python
print(6 ^ 3)
```

The binary representation of 6 is 0110
The binary representation of 3 is 0011

Then the ^ operator compares the bits and returns 0101, which is 5 in decimal.

## Operator Precedence

Operator precedence determines the order in which operations are performed in an expression.

Multiplication vs Addition

```python
print(100 + 5 * 3)  # Output: 115
```

Multiplication has higher precedence than addition, so it is performed first:
`5 * 3 = 15`, then `100 + 15 = 115`.

| Operator                                                         | Description                                       |
| ---------------------------------------------------------------- | ------------------------------------------------- |
| `()`                                                             | Parentheses                                       |
| `**`                                                             | Exponentiation                                    |
| `+x`, `-x`, `~x`                                                 | Unary plus, unary minus, bitwise NOT              |
| `*`, `/`, `//`, `%`                                              | Multiplication, division, floor division, modulus |
| `+`, `-`                                                         | Addition and subtraction                          |
| `<<`, `>>`                                                       | Bitwise left and right shifts                     |
| `&`                                                              | Bitwise AND                                       |
| `^`                                                              | Bitwise XOR                                       |
| `|`                                                              | Bitwise OR                                        |
| `==`, `!=`, `>`, `>=`, `<`, `<=`, `is`, `is not`, `in`, `not in` | Comparisons, identity, and membership operators   |
| `not`                                                            | Logical NOT                                       |
| `and`                                                            | Logical AND                                       |
| `or`                                                             | Logical OR                                        |

When two operators have the same precedence, the expression is evaluated from left to right.

Addition and subtraction have the same precedence. Therefore, we evaluate the expression from left to right.

```python
print(5 + 4 - 7 + 3)  # 5, because evaluation is left to right:
                      # (5 + 4) = 9
                      # 9 - 7 = 2
                      # 2 + 3 = 5
```

---

[<- Previous: Booleans](Booleans.md) | [Next: Lists ->](Lists.md) | [Table of Contents](../README.md)
