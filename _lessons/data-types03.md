---
layout: lesson
title: Using operators
unit: data-types
order: 2
feature-img: "assets/img/gradients/blue.png"
---

# Using operators

Remember that **values** are **assigned** to **variables**. Think of a variable as a named container for a value.

## Storing values in variables

Use variables to store and refer to data in your programs.

The single equal `=` syntax **assigns** a value to a variable.

```python
planet = 'Neptune'          # string
orbital_period_years = 165  # integer
mass_ratio_to_earth = 17.15 # float
is_inner_planet = False     # boolean
```

A variable can hold any type of value.

## Checking the type of a variable

Python programmers often rely on variable names and context about the problem and solution domain to know what data type a variable's value should be.

You can also use the built-in method `type()` to check the type of any value.

```python
planet = 'Neptune'
type(planet)                 # <class 'str'>
orbital_period_years = 165  
type(orbital_period_years)   # <class 'int'>
mass_ratio_to_earth = 17.15 
type(mass_ratio_to_earth)    # <class 'float'>
is_inner_planet = False     
type(is_inner_planet)        # <class 'bool'>
```

Variables do not specify a data type. Variables do not enforce a data type.

A variable can be **reassigned** to another value, even of a different type.

```python
planet = 'Neptune'
type(planet) # <class 'str'>
planet = 8
type(planet) # <class 'int'>
# planet = 8
# planet was a string, then it was reassigned to an integer
```

## Using the None object

If you plan to assign a value to a variable later in your program, try to choose a sensible default value.

```python
# surely, there are downsides to defaulting someone's age to 21
your_age = 12
# later determine the user's actual age
```

You can also use a special object `None` to indicate that the variable has not been assigned yet

```python
# wouldn't want to assume they are 12 either
your_age = None
# later determine the user's actual age
type(your_age) # <class 'NoneType'>
```

In fact, the `None` object is its own type.

## Understanding types and classes

You may have noticed that the `type()` function shows that these values belong to their own `class`. For many programs you write in Python, it is okay to not worry about the difference between type and class. If you are curious, you can read more about it in [this StackOverflow article.](https://stackoverflow.com/questions/35958961/class-vs-type-in-python)

A class is a categorization of objects that all behave similarly. Based on their class, objects can take on certain values, have certain attributes, and work with certain methods.

Programmers can even define their own custom classes. For now, you can still accomplish a great deal using built-in classes.
