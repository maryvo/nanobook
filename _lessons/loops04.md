---
layout: lesson
title: Looping over different types of values
unit: loops
order: 4
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Looping over different types of values

You can write loops that use other types of data besides numbers. Any type of data that can be looped over is described as an **iterable**. Lists and strings are examples of common iterables.

## Lists

You can loop over any list:

**Code**

```python
boolean_list = [True, False, False, False]
for boolean_value in boolean_list:
    if boolean_value:
        print('This one is True!')
    else:
        print('This one is False...')
```

This list has four items, so the loop body will run four times.

**Output**

```
This one is True!
This one is False...
This one is False...
This one is False...
```

## Strings

A string is a sequence of characters, which means you can loop over it too!

**Code**

```python
word = 'HAPPY'
for letter in word:
    print(letter)
print('I love my job.')
```

This string has five characters, so the loop body will run five times.

**Output**

```
H
A
P
P
Y
I love my job.
```
