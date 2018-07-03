---
layout: page
title: Building Blocks of Programs
subtitle: Learn Python through bite-sized modules.
feature-img: "assets/img/gradients/orange.png"
hide: true
---

# Guide Overview

In programming, **syntax** is the text that we write to create a program and **semantics** is the meaning or goal of that code. This guide is a starting place to help you write the syntax you need.

Each section in this guide covers a syntactical construct. Sections may include:

- The goal of the construct
- The syntax for using the construct
- Examples that you can run through step by step
- Links for further reading

## How to Read Code in this Guide

- When reading example syntax, words in `ALL_CAPS` represent places in the code that you fill in with custom text.
- Lines that start with a hashtag are comments. They do not get evaluated. Comments are used to explain code.

# Table of Contents

| Syntax (Construct)                                       | Semantics (Goal)                                   |
|----------------------------------------------------------|----------------------------------------------------|
| [1. Variables and Data Types](#variables-and-data-types) | Store data in a program.                           |
| [2. Input and Output](#input-and-output)                 | Bring data in and out of a program.                |
| [3. Conditional Statements](#conditional-statements)     | Select what part of a program should be run.       |
| [4. For Loops](#for-loops)                               | Repeat actions a set number of times.              |
| [5. While Loops](#while-loops)                           | Repeat actions as long as condition is true.       |
| [6. Functions](#function)                                | Group parts of a program related to a common task. |
| [7. String Manipulation](#string-manipulation)           | Store and retrieve information using text.         |

## Variables and Data Types

**Goal:** Store data in a program.

Programmers use **values** to represent data and **variables** to keep track of values.

Here is the syntax for assigning a value to a variable:

```python
VARIABLE = VALUE
```

Values can come from two places:

- Literal values, which are defined in the code
- Return values, which are returned by functions (see section 7)

There are four primitive types of values:

- Integers for whole numbers such as `1`, `-20`, and `0`
- Floats for fractional values such as `0.25` and `-1.333`
- Strings for text such as `'I enjoy coding'` and `'A'`
- Booleans for values that are either `True` or `False`

Here is the syntax for defining each type as a literal value:

```python
sample_string = 'I like Tacos.'
sample_integer = 42
sample_float = 7.61
sample_boolean = True
```

## Input and Output

**Goal:** Bring data in and out of a program.

Here is the syntax for taking user input:

```python
VARIABLE = input(PROMPT)
```

- Calling the `input()` function causes the program to display the (optional) `PROMPT` text (which must be a string) to the user and wait until they have entered some text.
- When the user writes text and hits enter, the program will store the text as a string in the `VARIABLE` and continue by executing the next line.
- Since the value from input will be a string, the programmer may have to convert it to another type.

Converting strings to numbers is the most common situation. Here are some examples:

```python
number_text = input('Enter a number: ')
# number_text = '24'
number = int(number_text)
# number = 24
```

```python
decimal_text = input('Enter a decimal: ')
# decimal_text = '1.76'
decimal = float(decimal_text)
# decimal = 1.76
```

Here is the syntax for output:

```python
print(MESSAGE)
```

- The `print()` function will display the `MESSAGE` text (which must be a string).

## Conditional Statements

**Goal:** Select what part of a program should be run.

Here is the syntax for writing a conditional statement:

```python
if CONDITION1:
    BRANCH_WITH_LINES_OF_CODE
elif CONDITION2:
    BRANCH_WITH_OTHER_LINES_OF_CODE
else:
    BRANCH_WITH_DIFFERENT_LINES_OF_CODE
```

- A **branch** of a conditional statement is run if and only if the condition above it is `True`.
- If no conditions are `True`, the else branch will run.
- Not all branches are required. It is possible to have a statement using just `if` or `if` and some number of `elif` without any `else` branch.

A **condition** is any operation or value that evaluates to `True` or `False`. Here are some example conditons:

```python
24 < 100 # True
3 + 7 == 10 # True
'cat' in 'catastrophe' # True
3 == 'dog' # False
```

You can read about more types of conditions here:

- [Comparing values](https://mimirhq.github.io/nanobook/lessons/conditionals02)
- [Using boolean operators](https://mimirhq.github.io/nanobook/lessons/conditionals03)

## For Loops

**Goal:** Repeat actions a set number of times.

Here is the syntax for writing a for loop:

```python
for VARIABLE_NAME in range(NUMBER):
    BODY_WITH_LINES_OF_CODE
```

- The **body** of the loop will be repeated `NUMBER` times.
- After that many runs, the program will continue by executing the next of code after the loop.

## While Loops

**Goal:** Repeat actions as long as condition is true.

Here is the syntax for writing a while loop:

```python
while CONDITION:
    BODY_WITH_LINES_OF_CODE
```

- The **body** of the loop will run as long as `CONDITION` is `True`.
- The condition will be evaluated each time, before the body is run.
- When the loop terminates, the program will continue by executing the next of code after the loop.

## Functions

**Goal:** Group parts of a program related to a common task.

Here is the syntax for defining a function:

```python
def FUNCTION_NAME(PARAMETERS):
    BODY_WITH_LINES_OF_CODE
    return RETURN_VALUE
```

- The function **body** contains all of the code to be run when the function is **called**.
- The function **parameters** are additional data for the function.
- Not all functions return a value. When the `return` statement is run, the function ends, and the program picks up execution at the next line after the function is called.
- A function may have one return statements, several return statements, or no return statements.
- If there are multiple return statements, only the first one to be run will take effect.

## String Manipulation

**Goal:** Store and retrieve information using text.

Coming soon...