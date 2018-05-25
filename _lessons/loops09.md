---
layout: lesson
title: Modifying items in a loop
unit: loops
order: 9
feature-img: "assets/img/gradients/blue.png"
---

# Modifying items in a loop

When using for loops, the loop counter variable or the item variable contains a copy of the value from the iterable. This means that if you modify the variable inside the for loop, it will not change the value that exists outside the scope of the loop body.

**Code**

```python
dogs = ['Golden Retriever', 'Great Dane', 'German Shepard']
for dog in dogs:
    dog = 'Corgi'
    print('I wish I had a ' + dog)
print(dogs)
```

**Output**

```
I wish I had a Corgi
I wish I had a Corgi
I wish I had a Corgi
['Golden Retriever', 'Great Dane', 'German Shepard']
```
