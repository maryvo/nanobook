---
layout: lesson
title: Looping with different step sizes
unit: loops
order: 2
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Looping with different step sizes

## The Range Function

**range(start, stop, [step])**

- `start`: Number to start range at (inclusive), default: `0`
- `stop`: Number to end range before (exclusive)
- `step`: The gap between each number in the range, default: `1`

The range() function only accepts integers, or whole numbers, so floating numbers, or numbers with decimals will cause a ```TypeError: 'float' object cannot be interpreted as an integer``` error to pop up.

## Step Size

The term **increment** means to add. You can change the incrementation of a loop with the `step` parameter.

**Code**

```python
# Count by fifty
for number in range(100, 350, 50):
    print(number)
```

**Output**

```
100
150
200
250
300
```

## Looping Backwards

Step size can also be negative, in case you want to loop backwards. This is called **decrementing** the loop counter.

**Code**

```python
for i in range(3, 0, -1):
    print(str(i) + "...")
print("Blast off!")
```

The line to print `"Blast off!"` is at the same indentation level as the start of the loop. This means that it is not part of the loop body and will only run once, after the loop finishes.

**Output**

```
3...
2...
1...
Blast off!
```

**Note**: If `stop` is less than `start` and `step` is not set to a negative value, the range will be empty.

```python
backwards = list(range(3, 0))
print(backwards)
# []
```
