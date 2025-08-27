# Welcome to Lab04 and Loops!

### Loops

In this lab, you will use loops in Python.

## Notes 

### Loops

Loops are used to repeat a block of code multiple times. There are two types of loops in Python: `for` loops and `while` loops.

### For Loops
For loops let you repeat a block of code a determined number of times. Here is an example of a for loop in Python:
```python   
for i in range(5):
    print(i)
```
> In this example, the code block `print(i)` will run 5 times. The variable `i` will start at 0 and end at 4.

### While Loops
While loops let you repeat a block of code as long as a condition is true. Here is an example of a while loop in Python:
```python
i = 0
while i < 5:
    print(i)
    i += 1
```
> In this example, the code block `print(i)` will run as long as the variable `i` is less than 5. The variable `i` will start at 0 and end at 4.


### Loops Cont.
Anything can be done inside a loop. You can have it print out strings, as show above. You can also have it do math, or even call a function. Here is an example of a loop that calls a function:
```python
def say_hello():
    print("Hello, World!")

for i in range(5):
    say_hello()
```


### Important Keywords
- `break` - This keyword is used to exit a loop.
- `continue` - This keyword is used to skip the current iteration of a loop and continue with the next iteration.

## Your Lab

|Part | Topic |
| --- | --- |
|A | For Loops|
|B | While Loops|

In this scenario, the grease from the fry trap got caught in Cashier-Bot's brain chip, and now he can't move! You will need to help him program a loop to get him to the other side of the room. 

**There are two different loops to try to see what will work for Cashier-Bot, but here is the general scenario for both:**
1. Cashier-Bot is in the center of the room, which is 100 units wide.
2. Cashier-Bot will flip a coin to determine if he will walk left or right.
3. Cashier-Bot will then take a random number of steps.
4. If Cashier-Bot reaches the wall, he wins!

We have provided you code to help you get started. It contains a function to flip a coin and get a random number of steps. (*Try printing out their results to see what they do!*)

**Some other things to note:**
- You have variables for the left wall and right wall. You can use these to check if Cashier-Bot has reached the wall.
- You have a variable for Cashier-Bot's position. You can use this to keep track of where Cashier-Bot is in the room.

> When submitting this lab, make sure both loops are included.

Copy the provided code below into your lab04.py file. You will need to complete the code to help Cashier-Bot walk to the other side of the room. 

### Part A ~ For Loops

For this loop, you will be using a `for` loop. The goal here is to run this loop 5 times to see if Cashier-Bot can reach either the right or left wall. If they do, they win! Otherwise, they will be told where they are in the room.

```python
# The random module is what let's us make calls to get random integers
import random

# This function simulates flipping a coin. It returns the string H for heads
# and T for tails
def flip_coin():
    coin = ''
    flip = random.randint(1, 10)
    if flip <= 5:
      coin = 'H'
    else:
      coin = 'T'
    return coin

# This function simulates taking a number of steps. It will return an integer
# number of steps to take
def get_steps():
    steps = random.randint(1, 50)
    return steps

# Use this variable to keep track of your position
position = 50
left_wall = 0
right_wall = 100

# TODO: Create a for loop to give yourself 5 chance to walk towards a wall
    # Flip a coin

    # Get number of steps
    
    # You can print the variable for coin and steps to help you debug  
    # print(coin, steps)

    # If coin flip is heads:
        # Walk right, i.e add steps to your position
    # Otherwise:
        # Walk left, i.e. remove steps from your position
      


# If you've reached either wall: you win
if position <= left_wall or position >= right_wall:
    print('You win!')
else:
    print('You are at position', position, 'in the room.')

```

### Part B ~ While Loops

For this loop, you will be using a `while` loop instead. The goal here is to run this loop over and over until Cashier-Bot reaches either the right or left wall. It will then print out how many chances it took to reach the wall.

```python
# Reset your position to the center of the room
position = 50

# Set your counter to see how many chances you have taken to reach the wall
counter = 0

# TODO: While you haven't reached the left wall or right wall:
    # Get a random number of steps
   
    # Flip a coin
    
    # Flip another coin
    
    
    # Debug print steps and coin flips
    # print out steps, coin1, and coin2

    # If the first coin toss is the same as the second:
        # Double the number of steps
    
    # If the first toss is heads:
        # Move right, add steps to your position
    # Otherwise:
        # Move left, subtract steps from your position


    # Increment your counter for each iteration    



# The following statement does not need to be changed.
print('You reached the wall after', counter, 'chances.')

# The code below is for us to test your code. Do not modify it.
assert(counter > 0)
assert(position <= left_wall or position >= right_wall)

```