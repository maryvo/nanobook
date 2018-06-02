---
layout: lesson
title: Selecting based on a value
unit: conditionals
order: 5
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Selecting based on a value

If you want to run a different branch of code based on the value of a variable, you can make an equality comparison in each `elif` branch. If the value is not one of the options you programmed in, then the `else` branch (if any) will run.

```python
# Get a string from standard input
animal = input('What is your favorite animal? ')
# run different code for each possible value
if animal == 'dog':
    print('I like dogs too!')
elif animal == 'cat':
    print('My friend likes cats too.')
elif animal == 'cow':
    print('Mooooo.')
elif animal == 'monkey':
    print('I hear they are very playful')
else:
    # run this code if none of the values match
    print('Interesting, what a cool animal!')
```
