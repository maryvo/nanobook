---
layout: lesson
title: Nesting branches
unit: conditionals
order: 4
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Nesting branches

You can include conditional statements inside other conditional statements.

## Indenting nested branches

Everything indented under a conditional statement belongs to its branch. Within a branch there can also be nested sub-branches. You can write as many nested conditionals as you can bare to read.

```python
if condition:
    # first branch
    if another_condition:
        # first sub-branch
    else:
        # second sub-branch
else:
    # second branch
    if yet_another_condition:
        # first sub-branch
    elif alternate_condition:
        # second sub-branch
    else:
        # third sub-branch
```

In the above example, exactly one of the five total sub-branches will run.

## Reading nested branches

Reading nested conditional statements follows the same process as reading normal conditional statements:

1. Read the top-level conditions in order from top to bottom
2. If a condition evaluates to `True`, start executing the code in its branch
3. Repeat this process for conditional statements in the branch

**Code**

```python
dessert = input('What kind of dessert would you like? ')
if dessert == 'ice cream':
    container = input('Would you like a cup or a cone?')
    if container == 'cone':
        print('Here is your ice cream in a cone.')
    elif container == 'cup':
        print('Here is your ice cream in a cup.')
    else:
        print('Sorry, we don\'t have that.')
elif dessert == 'cake':
    slices = int(input('How many slices would you like?'))
    if slices <= 0:
        print('You\'re gonna be real hungry.')
    else:
        print('Here is your cake.')
else:
    print('Sorry, we don\'t have that.')
```

Here are some input/output examples that show how the branches are evaluated:

**Output**

```
What kind of dessert would you like? cake
How many slides would you like? 4
Here is your cake.
```

**Output**

```
What kind of dessert would you like? ice cream
How many slides would you like? plate
Sorry, we don't have that.
```

**Output**

```
What kind of dessert would you like? churro
Sorry, we don't have that.
```

## Converting nested branches

Sometimes, it will make sense to write program logic using nested branches. But, this code may become long, repetitive, or confusing to read or debug later. You can use boolean operators to reduce nesting.

**Nested Code**

```python
your_age = 25 # in years
your_height = 61 # in inches
if your_age >= 13:
    if your_height >= 40:
        print('You are allowed to ride this roller coaster.')
    else:
        print('Sorry, you are not allowed to ride this roller coaster.')
else:
    print('Sorry, you are not allowed to ride this roller coaster.')

```

In this example, the age and height conditions can be combined into one condition with `and`:

**Non-Nested Code**

```python
your_age = 25 # in years
your_height = 61 # in inches
if your_age >= 13 and your_height >= 40:
    # run code only if both conditions are True
    print('You are allowed to ride this roller coaster.')
else:
    print('Sorry, you are not allowed to ride this roller coaster.')
```

Both code examples will have the same output.
