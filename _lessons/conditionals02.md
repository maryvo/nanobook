---
layout: lesson
title: Comparing values
unit: conditionals
order: 2
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Comparing values

Now that you have seen how to select branches based on a condition, you can learn more kinds of conditions to use. One common condition is a **comparison** between two values.

## Inequality comparisons

Here are some examples of inequality comparisons and how to read them:

|-----------------|-------------|--------|
| Inequality Code | Translation | Result |
|-----------------|-------------|--------|
| `2 < 3` | `2` is less than `3` | `True` |
| `1 > 400` | `1` is greater than `400` | `False` |
| `20 <= 30` | `20` is less than or equal to `30` | `True` |
| `50 >= 50` | `50` is greater than or equal to `50` | `True` |

### Inequalities with strings

You can also use inequality comparisons with strings. The comparison is based on the alphabetical order of the words.

|-----------------|-------------|--------|
| Inequality Code | Translation | Result |
|-----------------|-------------|--------|
| `'alpha' < 'beta'` | `'alpha'` is less than `'beta'` | `True` |
| `'dog' >= 'doggy'` | `'dog'` is greater than `'doggy'` | `False` |

## Equality comparisons

Check if two values are the same with the double equal `==` syntax.

```python
your_pet = 'dog'
my_pet = 'dog'
if your_pet == my_pet:
    print('Oh boy! We have the same kind of pet!')
```

A single equal symbol is an **assignment**, not a **comparison**. Python will warn you if you use the wrong symbol by providing a `SyntaxError` message like this:

```
>>> if 2 = 3:
  File "filename.py", line 1
    if 2 = 3:
         ^
SyntaxError: invalid syntax
```

You can also check if two values are not the same with the `!=` syntax.

```python
today = 'Thursday'
if today != 'Wednesday':
    print('Sadly, it is not hump day.')
```

## Identity comparisons

You can check if two variables refer to the same object with the `is` syntax. When working with primitive data types, use `==` instead of `is`.

If you want to check if a variable is `None`, then you should use `is`.

```python
if light_setting is None:
    print('The user has not chosen a light setting.')
```

## Saving a comparison to a variable

Every comparison generates a boolean value, so you can assign that boolean to a variable.

```python
birth_year = 2001
born_after_2000 = birth_year > 2000
if born_after_2000:
    print('You were born in the new millennium!')
```
