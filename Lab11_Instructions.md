# Welcome to Lab11 and Turtles!

### Turtles
In this lab, you will practice recursion using the turtle module in Python. Make sure to read everything thoroughly and send me a message if you have any questions!

## Notes

### What is the turtle module?
The turtle module is a graphics library that allows you to create pictures and shapes. It is a great way to learn about recursion and how it can be used to create complex shapes.

### Turtle Commands
Here are a few commands that you can use with the turtle module:
- `forward(distance)`: Moves the turtle forward by the specified distance.
- `backward(distance)`: Moves the turtle backward by the specified distance.
- `right(angle)`: Turns the turtle to the right by the specified angle.
- `left(angle)`: Turns the turtle to the left by the specified angle.
- `penup()`: Lifts the pen off the canvas so that the turtle does not draw.
- `pendown()`: Puts the pen back on the canvas so that the turtle can draw.
- `speed(speed)`: Sets the speed of the turtle. The speed can be a number from 1 to 10.

This is just scratching the surface of what you can do with the turtle module. You can learn more about it here: [Turtle Documentation](https://docs.python.org/3/library/turtle.html)

### Recursion in the Turtle Module
Recursion can be used to create complex shapes with the turtle module. By calling a function recursively, you can create intricate patterns and designs.

We're going to be using the turtle module to explore something called a Koch snowflake. 

#### What is a Koch Snowflake?
A Koch snowflake is a fractal that is created by starting with an equilateral triangle and adding smaller equilateral triangles to each side. This process is repeated indefinitely, creating a snowflake-like shape.

Here is an example of a Koch snowflake:

![Koch Snowflake](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/KochFlake.svg/1024px-KochFlake.svg.png?20220529063320)

Notice how we start with 1 triangle, then add 3 triangles to it's side. Then, each of those triangles has 2 more triangles added to their sides, and so on.

We can use recursion here to take those one large shape and break it down into smaller shapes.

## Your Lab

|Part | Topic |
| --- | --- |
|A | Getting to Know Turtle|
|B | Koch Snowflake|

### Part A ~ **Getting to Know Turtle**

In this part, you will practice using the turtle module to draw shapes.

```python
from turtle import *
def draw_square(length):
    #right now this function draws a line, update it iteravely to draw a square
    forward(length)
    right(90)

speed(0)
penup()
goto(-200, 100)
pendown()
draw_square(50)
done()

```

If you want to play around with Turtle more, try creating functions to draw other shapes like triangles, pentagons, or hexagons!

### Part B ~ **Koch Snowflake**

Using the starter code below, implement the function `koch_fractal` that will draw a Koch snowflake using recursion. The function should take two arguments: 
1. `n`, which is the number of turns the turtle should make
2. `step`, which is the distance the turtle should move forward

Note: The code **below** the function definition is used to draw the snowflake. You do not need to modify it. However, you can modify the function call itself.

```python
from turtle import *
def koch_fractal(n, step):
    # Base case: if no turns (n) remain,
    if n == 0:
        # TODO: walk forward step amount

        return


    # START Recursive case

    # TODO: Draw fractal with one fewer turns by decreasing n
    # Keep the step size the same


    # TODO: Have Turtle turn left 60 degrees


    # TODO: Draw fractal with one fewer turns by decreasing n
    # Keep the step size the same


    # TODO: Have Turtle turn right 120 degrees


    # TODO: Draw fractal with one fewer turns by decreasing n
    # Keep the step size the same


    # TODO: Have Turtle turn left 60 degrees


    # TODO: Draw fractal with one fewer turns by decreasing n
    # Keep the step size the same


    # END recursive case

# This brings Turtle to leftmost portion
# of screen. You do not need to change this code.
title("Koch Fractal")
speed(0)
penup()
goto(-200, 100)
pendown()

# Here you can change calls to koch_fractal to draw curves
# Remember the first argument n is how many turns you want
# Turtle to make drawing curves, and the second argument step
# is how far Turtle will walk forward.
# This function is not efficient, so try with small values of n
# Optional: Make a snowflake by combining 3 koch fractals into a triangle
koch_fractal(4, 10)

hideturtle()
done()
```

### Debugging

There are a few common errors that you might encounter when working with the turtle module:
1. Forgetting to import the turtle module: Make sure you import the turtle module at the beginning of your code. Make sure you have `from turtle import *` at the top of your code.
2. The window may not pop infront of VSCode. If you are using VSCode, you may need to click on the turtle window to bring it to the front.
3. It's okay if your drawing does not match the images above exactly. The goal is to get a sense of how recursion can be used to create complex shapes.
4. If you run into a No module named '_tkinter' error, you’ll have to install the Tk interface package on your system. If you see this error, please head to the lab to get some assistance from a TA. It'll be a little involved and it's best to ask for help here.