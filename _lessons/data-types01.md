---
layout: lesson
title: Types of data
unit: data-types
order: 1
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Types of data

Programs represent concepts from a certain **problem domain** in their own **solution domain**. When you model elements of the problem you want to solve in your code, you choose types of data.

We use **values** to represent data and **variables** to keep track of values.

All values in Python are **objects**. The **type** or **class** of an object determines what values it can take on, what attributes it has, and what functions it is compatible with.

## Choosing between primitive types

In Python, you can work with four **primitive** data types:

- Integers for whole numbers such as `1`, `-20`, and `0`
- Floats for fractional values such as `0.25` and `-1.333`
- Strings for text such as `'I enjoy coding'` and `'A'`
- Booleans for values that are either `True` or `False`

The single equal `=` syntax **assigns** a value to a variable.

```python
planet = 'Neptune'          # string
orbital_period_years = 165  # integer
mass_ratio_to_earth = 17.15 # float
is_inner_planet = False     # boolean
```

## Declaring variables with initial values

When values are written into a program literally, the syntax determines their type. Putting quotation marks around a value will **declare** it as a string. Using a floating point (decimal point) will declare a numerical value as a string.

```python
# declaring an initial string value and assigning it to a variable
planet = 'Neptune'
```

Booleans must be capitalized. Otherwise you will get a `NameError` because the computer thinks you are referencing a variable named `false`.

```python
is_inner_planet = false
```

```
  File "filename.py>", line 1
NameError: name 'false' is not defined
```

**Note:** Only suffering can come from actually naming a variable `false`.

Other errors in the syntax of declaring a value can also cause `NameError`s and `SyntaxError`s. But, it is better to have a known error that you can fix than to accidentally use the wrong data type and have to figure out why a program is misbehaving.
