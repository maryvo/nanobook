---
layout: lesson
title: Using boolean operators
unit: conditionals
order: 3
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Using boolean operators

You can combine simple conditions to create more complex or specific conditions. To do this, learn how to use and read the boolean operators: `and`, `or`, and `not`.

## Satisfying both conditions

To check if two conditions are both `True`, use the `and` operator:

```python
your_age = 25 # in years
your_height = 61 # in inches
if your_age >= 13 and your_height >= 40:
    # run code only if both conditions are True
    print('You are allowed to ride this roller coaster.')
```

## Satisfying at least one condition

To check if at least one condition is `True`, use the `or` operator:

```python
sunny_outside = False
nobody_is_home = True
if sunny_outside or nobody_is_home:
    # run code only if at least one condition is True
    turn_off_lights()
```

The `or` operator will return `True` if one or both conditions are `True`.

Consider this **truth table**, showing every possible combination of values:

|-----------------|----------------|-----------------------------------|-----------------------------|
| Value of `sunny_outside` | Value of `nobody_is_home` | Result of `sunny_outside or nobody_is_home` | Should the lights turn off? |
|-----------------|----------------|-----------------------------------|-----------------------------|
| `True`  | `True`  | `True`  | Yes |
| `True`  | `False` | `True`  | Yes |
| `False` | `True`  | `True`  | Yes |
| `False` | `False` | `False` | No  |

## Negating a boolean

To flip the value of a condition, use the `not` operator:

```python
battery_percentage = 71 # percent
low_battery = battery_percentage <= 25
if not low_battery:
    # run code only if the opposite of the condition is True
    increase_brightness()
```

## Reading boolean operations

You can use boolean operations on more than two conditions. To make it easier to understand and read, it is best to evaluate booleans in pairs.

Consider this example where three conditions influence the outcome:

```python
sunny_outside = False
nobody_is_home = True
energy_saving_mode_on = True
if (sunny_outside and nobody_is_home) and energy_saving_mode_on:
    turn_off_lights()
```

To read this condition, we will use parentheses to determine the order of evaluation.

1. Evaluate: `(sunny_outside and nobody_is_home)`.
2. The `and` operator requires both conditions to be `True`. Since `sunny_outside` is `False`, this expression results in `False`
3. Replace the expression in parentheses with its result.
4. Evaluate the simplified expression: `(False) and energy_saving_mode_on`.
5. Again, `and` requires both conditions to be `False`. This expression results in `False`.
6. The final result is `False`.
