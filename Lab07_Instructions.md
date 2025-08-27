# Welcome to Lab07 and Data Structures!

### Data Structures

In this lab, you will explore data structures and call stacks.

## Notes 

### Data Structures
There are many different data structures in Python. Here are a few:
- Lists
- Tuples
- Dictionaries
- Sets

However, this only begins to scratch the surface of data structures. Conceptually, there are many more. Now, for the purposes of this class, you won't have to go into too much detail about data structures. However, it is important to know that they exist and that they are used in programming.

Some other data structures include:
- Stacks
- Queues
- Trees
- Graphs
- Heaps
- And many more!

### Stack Diagram
A call stack is a stack data structure that stores information about the active subroutines of a computer program. This is important because it allows the program to keep track of where it is in a program.

For the purposes of this class, however, we're going to keep things simple.

## Your Lab

|Part | Topic |
| --- | --- |
|A | Stack Diagram |


## Part A ~ **Stack Diagram**

For this lab, you will need to submit a drawing of a stack diagram. This diagram should trace the program below. You can draw this by hand or use a drawing tool. 

```python
def secret_math(x):
    secret_num = subtract_3(x)
    return secret_num * 2

def subtract_3(y):
    return y - 3

num = 5
result = secret_math(num)
```
