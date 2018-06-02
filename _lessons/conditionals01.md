---
layout: lesson
title: Selecting a branch to execute
unit: conditionals
order: 1
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Selecting a branch to execute

## Indenting code for conditional statements

Indentation allows you to organize your program into **branches**: blocks of code that can be selected based on conditions.

```python
if condition:
    # first branch
    # this code will only execute if condition is true
    # more code
else:
    # second branch
    # this code will only execute if the first branch condition is not true
    # more code
```

## Selecting between two branches

If the first condition is not true, you can run some other branch with the `else` syntax.

```python
sunny_outside = True
if sunny_outside:
    print('Let\'s go to the beach!')
else:
    print('Let\'s stay inside...')
```

## Selecting between multiple branches

If you have multiple branches to choose from, you can set a condition for each one using the `elif` syntax.

```python
your_age = 12 # in years
if your_age >= 20:
    # first branch to run only if its condition is true
    print('You are too old for the teen area.')
elif your_age < 13:
    # additional branch to run only if is condition is true
    print('You are too young for the teen area.')
else:
    # final branch to run only if none of the above conditions are true
    print('Welcome to the teen area!')
```

## Executing conditional code in your head

To execute conditional code in your head, follow these steps:

1. Read each conditional statement in order from top to bottom
2. Determine if the condition is true
3. If the condition is true, execute the indented code in its branch and skip all other branches
4. If the condition is not true, continue to the next branch
5. If you reach the else branch, execute the indented code
