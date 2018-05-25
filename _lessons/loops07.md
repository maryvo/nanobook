---
layout: lesson
title: Identifying infinite loops
unit: loops
order: 7
feature-img: "assets/img/gradients/blue.png"
toc: true
---

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
