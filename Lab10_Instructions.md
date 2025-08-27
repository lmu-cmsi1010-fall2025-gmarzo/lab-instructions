# Welcome to Lab10 and Recursion!

### Recursion

In this lab, you will practice concepts around recursion and use it in your code.

## Notes 

### What is recursion?
Recursion is a method of solving problems that involves breaking a problem down into smaller and smaller subproblems until you get to a small enough problem that it can be solved trivially. Usually recursion involves a function calling itself. While it may not seem like much on the surface, recursion allows us to write elegant solutions to problems that may otherwise be very difficult to program.

### Recursion in Python
In Python, a recursive function is a function that calls itself. To prevent infinite recursion, you must include a base case that stops the recursion. The base case will end the recursive calls.

For example, the following function calculates the factorial of a number using recursion:

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
```

### Base Case
The base case is the condition that stops the recursion. It is the simplest form of the problem that can be solved directly. The base case acts as the exit condition for the recursive function. The base case in the above example is `if n == 0:`.

### Recursive Case
The recursive case is the condition that calls the function recursively. It is the part of the function that calls itself with a modified input. The recursive case in the above example is `return n * factorial(n-1)`.


## Your Lab

|Part | Topic |
| --- | --- |
|A | Stack Diagram|

### Part A ~ Stack Diagram
We taklked about stack diagrams a few weeks ago. In this part, you will create a stack diagram for the following recursive function:

```python
def mystery(n):
    if n == 0:
        return 0
    else:
        return n + mystery(n-1)
```

#### Create a stack diagram for the function `mystery(3)`.

