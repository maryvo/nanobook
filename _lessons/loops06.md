---
layout: lesson
title: Terminating loops early
unit: loops
order: 6
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Terminating loops early

## Terminating for loops

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

## Terminating while loops

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

## Terminating nested loops

If you use the `break` keyword, it will only break out of the current loop. The outer loop will still continue, unless it also hits a break statement.

**Code**

```python
# Which states have more than one vowel in a row?
states = ['Indiana', 'New York', 'Louisiana', 'Colorado', 'Denver']
vowels = 'aeiou'
for state in states:
    print('Checking: ' + state)
    previous_was_vowel = False
    for letter in state:
        is_vowel = letter.lower() in vowels
        if is_vowel and previous_was_vowel:
            print('- Yes, it has consecutive vowels!')
            break
        previous_was_vowel = is_vowel
print('All done!')
```

**Output**

```python
Checking: Indiana
- Yes, it has consecutive vowels!
- Moving on to the next state...
Checking: New York
- Moving on to the next state...
Checking: Louisiana
- Yes, it has consecutive vowels!
- Moving on to the next state...
Checking: Colorado
- Moving on to the next state...
Checking: Denver
- Moving on to the next state...
All done!
```

After the `break` statement, execution will continue after the end of the nested loop. That is why the `- Moving on to the next state...` gets printed on every iteration of the outer loop.
