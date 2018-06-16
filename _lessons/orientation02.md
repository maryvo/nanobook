---
layout: lesson
title: How can I learn to code?
unit: orientation
order: 2
feature-img: "assets/img/gradients/blue.png"
toc: true
---

# How can I learn to code?

Learning to code may feel different from other skills you have learned. Here is an overview of what programming includes.

## Solving programming problems

One theory [1] suggests that successful programmers repeat these six steps when faced with a problem:

1. Interpret the problem
2. Think of similar problems
3. Think of potential solutions to the problem
4. Evaluate potential solutions
5. Implement a solution
6. Evaluate the implementation of the solution

> 1. Loksa, Dastyni & Ko, Andrew. (2016). The Role of Self-Regulation in Programming Problem Solving Process and Success. 83-91.

## Reading programs

Many people emphasize learning to write code. But reading code is just as important, if not more important. You will need to read code in order to:

- Understand how some code works
- Understand the implications of some code
- Search for errors in some code
- Explain some code that another person wrote
- Explain some code that you wrote
- Learn new ways of using code

To learn to read and write code better, you will build a **Notional Machine** in your head. This machine is a mental model of how computer programs work. It will help you tell the difference between:

- **Syntax:** the symbols we use to write programs
- **Semantics:** the meaning we actually want to communicate

This is part of the challenge in learning to program. You will have a goal in your head. The computer cannot understand this goal until you choose the right syntax and programming concepts to give it good instructions.

## Writing programs

### Reading starter code

Blank code editors are scary. Taking a problem in the real world and transforming it into a solution written in code is challenging. In many coding exercises you will be given instructions and starter code to make it easier to get started.

But sometimes, that starter code can also be confusing. Here are some tips for reading starter code:

- Read the starter code and all code comments before writing your own code
- Read the problem instructions and try to identify how each function name, variable, or other syntax relates to the problem description
- If you are allowed to change variable names, feel free to change them to names that make more sense to you
- Usually, you are not allowed to change the name of starter functions

### Debugging code

Every single programmer runs into **bugs**: issues of any size that prevent programs from working correctly.

- **Syntax** bugs come from code that is written incorrectly and cannot be understood by the computer
- **Semantic** bugs arise when the meaning of the code does match the intentions of the programmer 

Bugs can be categorized in many other ways. As you read and write more programs, you will develop the skills of identifying and fixing bugs.

#### Reading an error trace

When you have an error in your code, the program error output offers feedback on what might be wrong. This output is called a **traceback**.

```
Traceback (most recent call last):
  File "filename.py", line 1
NameError: name 'me' is not defined
```

The traceback tells you:

- What kind of error the program detected
- What file the error may be from
- What line number the error may be at
- Additional details about the error
