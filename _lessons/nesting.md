---
layout: lesson
title: Nesting
unit: loops
order: 3
feature-img: "assets/img/gradients/blue.png"
toc: true
---

Writing loops inside other loops is called nesting.

# Nesting for loops

An **inner loop** is **nested** inside the body of an **outer** loop. Each time the outer loop _body_ runs an **iteration**, the entire inner loop runs.

Inner loops can access variables that are inside the outer loops they are nested in.

**Code**

```python
# 3x3 multiplication table
for a in range(1, 4):
    # Body of loop a
    for b in range(1, 4):
        # Body of loop b
        product = a * b
        print(str(a) + ' x ' + str(b) + ' = ' + str(product))
```

**Output**

```
1 x 1 = 1
1 x 2 = 2
1 x 3 = 3
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
```

- The body of loop a, by itself, will run 3 times
- The body of loop b, by itself, will run 3 times
- Since loop b is nested inside loop a, loop b will run 3 times
- So, the body of loop b will end up running 3 x 3 = 9 times in total

Suppose we change the range of loop b to `range(1, 11)`:

- The body of loop b, by itself, will run 10 times
- So, the body of loop b will end up running 3 x 10 = 30 times in total

You can triple-nest loops. You can quadruple-nest loops. You can nest as many times as you need to.

**Code**
```python
for x in range(3):
    for y in range(10):
        for u in range(4):
            for v in range(7):
                print(x, y, u, v)
```

- The body of loop x will run 3 times in total
- The body of loop y will run 3 x 10 = 30 times in total
- The body of loop u will run 3 x 10 x 4 = 120 times in total
- The body of loop v will run 3 x 10 x 4 x 7 = 840 times in total

You can also nest while loops in any way you like. But with while loops, you may not be able to count exactly how many times nested loops will run.

# Terminating nested loops

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
