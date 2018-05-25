---
layout: lesson
title: Accessing positions of items in a loop
unit: loops
order: 8
feature-img: "assets/img/gradients/blue.png"
---

# Accessing positions of items in a loop

Every item in an iterable also has an **index**, starting from `0`, that indicates its position. You can access every item and its index by **enumerating** the items.

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
