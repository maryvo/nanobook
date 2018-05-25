---
layout: lesson
title: Repeating actions for a range of numbers
unit: loops
order: 1
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Repeating actions for a range of numbers

For loops repeat some code for every item in a sequence.

## Repeating tasks using loops

The first line of a loop tells the computer how many times the loop will run. Each turn is called an **iteration**.

The **body** of the loop is any code that is indented past the loop's first line. The body gets repeated on each iteration.

In the example below, the variable `i` is called the loop **counter** because it keeps track of which iteration we are on.

**Code**

```python
for i in range(3):
    # This is the body
    print(i)
    # This will print three times
```

**Output**

```
0
1
2
```

Surprised that the number 3 never printed? Read on.

## Changing the loop range

Ranges allow you to specify how many times to run a loop. By default, a range starts at zero. But you can change that!

### The Range Function

**range(start, stop, [step])**

- `start`: Number to start range at (inclusive), default: `0`
- `stop`: Number to end range before (exclusive)
- `step`: The gap between each number in the range, default: `1`

The `range()` function returns a value of type `range`. The range contains numbers between `start` and `stop`, but does not include `stop`.

If only one parameter is given to `range()`, it will be used as the value for `stop`.

The `range` type is different from the `list` type, but you can convert a range to a list to see what numbers it contains:

```python
numbers = list(range(3, 7))
print(numbers)
# [3, 4, 5, 6]
```
