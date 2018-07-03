# Building Blocks of Programs

## Guide Overview

In programming, **syntax** is the text that we write to create a program and **semantics** is the meaning or goal of that code. This guide is a starting place to help you write the syntax you need.

Each section in this guide covers a syntactical construct. Sections may include:

- The goal of the construct
- The syntax for using the construct
- Examples that you can run through step by step
- Links for further reading

### How to Read Code in this Guide

- When reading example syntax, words in `ALL_CAPS` represent places in the code that you fill in with custom text.
- Lines that start with a hashtag are comments. They do not get evaluated. Comments are used to explain code.

## Table of Contents

| Syntax (Construct)            | Semantics (Goal)                                   |
|-------------------------------|----------------------------------------------------|
| 1. Variables and Data Types   | Store data in a program.                           |
| 2. Input and Output           | Bring data in and out of a program.                |
| 3. Conditional Statements     | Select what part of a program should be run.       |
| 4. For Loops                  | Repeat actions a set number of times.              |
| 5. While Loops                | Repeat actions as long as condition is true.       |
| 6. String Manipulation        | Store and retrieve information using text.         |
| 7. Functions                  | Group parts of a program related to a common task. |

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

```python
name = input('What is your name? ')
print('Hello')

```

## Conditional Statements

**Goal:** Select what part of a program should be run.

Here is the syntax for writing a conditional statement:

```python
if CONDITION1:
    LINES_OF_CODE
elif CONDITION2:
    OTHER_LINES_OF_CODE
else:
    DIFFERENT_LINES_OF_CODE
```

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
    do_something()
```

## While Loops

**Goal:** Repeat actions as long as condition is true.

Here is the syntax for writing a while loop:

```python
while CONDITION:
    do_something()
```

## String Manipulation

**Goal:** Store and retrieve information using text.

Coming soon...

## Functions

**Goal:** Group parts of a program related to a common task.

Here is the syntax for defining a function:

```python
def FUNCTION_NAME():
    do_something()
    return RETURN_VALUE
```