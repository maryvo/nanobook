---
layout: lesson
title: For Loops
unit: loops
order: 1
feature-img: "assets/img/gradients/blue.png"
toc: true
---

For loops repeat some code for every item in a sequence.

# Repeat tasks using loops

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

# Change the loop range

Ranges allow you to specify how many times to run a loop. By default, a range starts at zero. But you can change that!

## Parameters

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

## Steps

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

# Loop over different kinds of values

You can loop over more than just numbers!

- **Sequences** contain ordered items
- **Collections** contain items that do not have a specified order

You will meet more examples of sequences and collections when we get to Data Structures. Here are some useful sequences:

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


# Access positions of items

Since sequences are ordered, every item has an **index**, starting from `0` to indicate its position. You can access every item and its index by **enumerating** the items.

**Code**

```python
# Printing my favorite desserts
favorites = ["Banana Split", "Chocolate Shake", "Vanilla Ice Cream"]
for (index, dessert) in enumerate(favorites):
    rank = index + 1
    print(str(rank) + '. ' + dessert)
```

**Output**

```
1. Banana Split
2. Chocolate Shake
3. Vanilla Ice Cream
```

# Terminate a loop early 

To exit a loop early and avoid running the remaining iterations, you can use the `break` keyword.

**Code**

```python
# Find an integer divisible by both 7 and 3
number = None
for i in range(1, 10000):
    if i % 3 == 0 and i % 7 == 0:
        number = i
        break
print('Found one: ' + str(number))
```

**Output**

```
Found one: 21
```
