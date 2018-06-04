---
layout: lesson
title: Working with lists of data
unit: data-types
order: 4
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# Working with lists of data

## Using operators on lists

Beyond primitive data types, there are **data structures**. A data structure is way of organizing data. In Python, the built-in data structures have names like `list`, `dictionary`, `set`, and `tuple`. We will consider data structures in more detail in the future, but for now, lists are a common data structure you will encounter when coding in Python.

The syntax for defining a list looks like this. The square brackets and commas separate the contents of a list.

```python
list_name = [value1, value2, value3]
```
Lists can contain values of any data type. Even different data types, although such lists can be confusing to programmers.

```python
number_list = [32, 56, 71, -12, 8, 43]
weird_list = [True, 3.6, 'sdasd', 12, False, 0.0003]
```

Just like with a string, you can use the `in` operator to check if a value is included in a list.

```python
value = 2
number_list = [32, 56, 71, -12, 8, 43]
search = value in number_list
# search = False
```

## Working with indexes

Every item in a list has both a **value** and a **position**. The position is represented by a integer number called the **index** which starts counting from zero.

You can access an item in a list using the square bracket index operator `[]`. The syntax looks like this:

```python
float_list = [2.3, 5.4, 6.7, 1.3]
second = float_list[1]
# second = 2.4
```

## Converting strings to lists

A string value is similar to a list because you can also retrieve individual **characters** of a string by their index.

```python
name = 'Troy'
name[1] # = r
```

If you need to convert a string to a list explicitly, you can use the conversion function:

```python
name = 'Troy'
letters = list(name)
# letters = ['T', 'r', 'o', 'y']
```

Be mindful that converting a list of any values to a string does not work in exactly the opposite way.

```python
letters = ['T', 'r', 'o', 'y']
list_string = str(letters)
# list_string = "['T', 'r', 'o', 'y']"
# the result is a string representing the contents of the list
numbers = [2, 3, 4]
numbers_list_string = str(numbers)
# numbers_list_string = '[2, 3, 4]'
# converting a list of integers also results in a string representing the contents of the list
```
