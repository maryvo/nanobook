---
layout: lesson
title: While Loops
unit: loops
order: 2
feature-img: "assets/img/gradients/blue.png"
toc: true
---

While loops continue looping as long as some condition is true.

# Repeating based on a condition

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

The condition for a while loop can be any boolean value. The boolean value can come from a comparison, a function, or practically anywhere else.

**Code**

```python
# Fictional methods about robotic submarines
while hull_integrity_is_safe():
    dive_deeper()
```

# Terminating a loop early

Just like with for loops, you can instruct the computer to exit a while loop early using the `break` keyword.

**Code**

```python
# Are there at least 5 numbers divisible by 7 that are less than 100?
i = 1
count = 0
while i < 100:
    if i % 7 == 0:
        count += 1
    if count >= 5:
        # No need to keep searching!
        break
    i += 1
if count >= 5:
    print('Yes, there are at least 5 such numbers')
else:
    print('No, there are less than 5 such numbers')
```

**Output**

```
Yes, there are more than 5 such numbers
```

# Identifying infinite loops

If the condition of a while loop is never met, the computer will keep running the loop body. Infinite loops will run forever, until the program is forcibly stopped. If you see an error message saying that a program **times out**, one possible cause is that the program contained an infinite loop and had to be terminated.

Here are a few issues to look for when trying to repair infinite loops.

## Conditions that are never satisfied

If the condition of a loop never evaluate to `False`, then it can never finish.

**Code:** Infinite Loop

```python
i = 1
while i < 50:
    i -= 1
print('All done!')
```

Since `i` is decremented on each iteration, it will never be less than 50. This loop will run forever and the `'All done!'` message will never be printed.

## Conditions that are sometimes satisfied

Even more sneaky: there are loops that will terminate regularly under some conditions and run infinitely under other conditions. If you the programmer do not control a value that the loop depends on, it may run infinitely.

**Code:** Possibly Infinite Loop

```python
print('We are going to count up to 100.')
increment = int(input('Count in multiples of: '))
number = 0
while number != 100:
    print(number)
    number += increment
print('We reached 100!')
```

**Output**: Terminates

```
We are going to count up to 100!
Count in multiples of: 25
0
25
50
75
We reached 100!
```

**Output**: Runs Forever

```
We are going to count up to 100!
Count in multiples of: 29
0
29
58
87
116
145
...
```

In the above example, a more sensible loop condition that would avoid looping infinitely could be:

```python
while number <= 100:
```

But if the value of `increment` were negative, then even that condition would not prevent an infinite loop!

## Break statements that are never reached

The most clear infinite loop is one that looks like this:

```python
while True:
    # Some loop body
```

Every time the loop condition is checked, it must be true. If you see a loop that looks like this you should immediately be suspicious.

Some programmers do use `while True:` loops. Remember our friend `break`? That can allow such loops to terminate instead of running forever.

**Code:** Terminating Loop

```python
print('I am spooked.')
scream = 'A'
while True:
    scream += 'a'
    if len(scream) > 10:
        scream += 'h!'
        break
print(scream)
```

**Output**

```
I am spooked.
Aaaaaaaaaaah!
```

But, if no break statement is ever reached in the loop, the loop cannot terminate.

**Code:** Infinite Loop

```python
print('I am spooked.')
scream = 'A'
while True:
    scream += 'a'
    if scream == "Aaaaah!":
        scream += 'h!'
        break
print(scream)
```

**Output**

```
I am spooked.
...
```

In the second version of the loop, the conditional check that guards the break statement will never result in `True`, so the loop will never exit.
