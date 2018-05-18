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

# Accessing variables in loops

Coming soon...
