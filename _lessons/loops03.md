---
layout: lesson
title: Repeating actions while a condition is true
unit: loops
order: 3
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Repeating actions while a condition is true

## Using while loops

While loops continue looping as long as some condition is true.

While loops are structured differently from for loops. Instead of repeating over a range or sequence, while loops repeat as long as they need to until some condition is met.

While loops can be useful when you want to repeat something but don't know exactly how many iterations are needed.

**Code**

```python
# What are all the square numbers less than 100?
number = 1
square = 1
while square < 100: # This is the loop condition
    # This is the loop body
    print(square)
    number += 1
    # This is where the condition can change
    square = number ** 2
```

**Output**

```
1
4
9
16
25
36
49
64
81
```

Before each new iteration of the loop body, the computer checks if the loop condition is true.

**Note:** If the condition is not true at the start of the loop, the body will never run!

## Validating user input with while loops

Another common application of while loops is getting user input. You can make your program repeatedly prompt users for input until they provide input that meets the desired conditions.

**Code**

```python
word = ''
while len(word) != 5:
    word = input('Give me a five letter word: ')
print('Yes, that works!')
```

**Output:** With User Input

```
Give me a five letter word: cow
Give me a five letter word: beaver
Give me a five letter word: elephant
Give me a five letter word: eagle
Yes, that works!
```

## While loops with any conditions

The condition for a while loop can be any boolean value. The boolean value can come from a comparison, a function, or practically anywhere else.

**Code**

```python
# Fictional methods about robotic submarines
while hull_integrity_is_safe():
    dive_deeper()
```
