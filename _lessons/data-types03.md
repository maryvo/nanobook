---
layout: lesson
title: Using operators
unit: data-types
order: 3
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Using operators

**Operations** are performed on data. **Operators** are syntax indicating what operation to perform.

## Using mathematical operators

When programming in Python, the mathematical operators you know and love work just as you might expect.

|-----------|----------|---------|--------|
| Operation | Operator | Example | Result |
| Addition       | `+` | `a = 2 + 2` | `# a = 4` |
| Subtraction    | `+` | `b = 3 - 4` | `# b = -1` |
| Multiplication | `+` | `c = 6 * 3` | `# c = 18` |
| Division       | `+` | `d = 8 / 2` | `# d = 4.0` |
| Exponentiation | `**` | `exp = 2 ** 2` | `# exp = 4` |

- Notice that the division of two integers results in a float.
- Computing the exponent uses the `**` operator. The `^` operator you may be used to means something different in Python.

You can also add strings. This is called **concatenation**.

```python
dollars = '$' + str(100) + ',' + str(500)
# dollars = '$100,500'
```

### Using integer division

There is also an integer division operation using the `//` operator that truncates the result to a whole number by rounding down. Consider these examples:

```python
# integer division always rounds down in the negative direction, not necessarily towards zero
7 // 3      # = 2
-7 // 3     # = -3
# integer division on float values does truncate, but preserves the float type
7.0 // 3.0  # = 2.0
-7.0 // 3.0 # = -3.0
# if even one of the two values in the operation is a float, the result will be a truncated float
7 // 3.0    # = 2.0
-7.0 // 3   # = -3.0
```

### Using modulo to find remainders

Another common operation is to find the remainder of a division. You can accomplish this with the modulo operator `%`.

```python
# check for remainder
37 % 5  # = 2
# if the remainder is 0, then the dividend is cleanly divisible by the divisor
dividend = 50
divisor = 10
remainder = dividend % divisor
# remainder = 0
```

## Reading operators

An **operator** applies an operation on the values to the left and right of the symbol. The result of the operation is a new value. Use precedence of operations and parentheses to determine the order in which operations are evaluated.

For example, multiplication has precedence over addition. In this example, the operator `*` is applied to `4` on its left and `3` on its right.

```python
val = 2 + 4 * 3
# val1 = 14
```
Using parentheses, the operator `*` is applied to `(2 + 4)` on its left and `3` on its right.

```python
val2 = (2 + 4) * 3
# val2 = 18
```

## Other operators

The mathematical operators are not the only kinds of operators. In most code editors, you will see the keywords and key symbols highlighted in a special color.

Operators can be keywords too, not just key symbols. Consider the `in` operator which checks if a smaller string is contained in a bigger string and returns a boolean with the result.

```python
message = 'I love doggos'
search = 'dog' in message
# search = True
```
