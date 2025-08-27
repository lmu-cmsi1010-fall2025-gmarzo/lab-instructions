# Welcome to Lab06 and Lists and Tuples!

### Lists and Tuples

In this lab, you will use lists in Python. 

## Notes 

### Lists
Lists are useful in Python to store multiple items in a single variable. It is a collection of items that are ordered and changeable. Lists are defined by having values between square brackets `[]`.
Here is an example of a list:
```python
grocery_list = ["apples", "bananas", "oranges"]
```
> In this example, the list `grocery_list` contains three strings: "apples", "bananas", and "oranges".

### Indexing
Just like strings, you can index into lists. Indexing starts at 0. Here is an example:
```python
grocery_list = ["apples", "bananas", "oranges"]
print(grocery_list[0])
```
> In this example, the code block `print(grocery_list[0])` will print "apples".

### Slicing
Just like strings, you can slice lists. Here is an example:
```python
grocery_list = ["apples", "bananas", "oranges"]
print(grocery_list[0:2])
```
> In this example, the code block `print(grocery_list[0:2])` will print `["apples", "bananas"]`.

### Methods
There are many, different methods for lists in Python. Here are a few:
- `append()` - This method adds an element to the end of the list.
- `remove()` - This method removes the first occurrence of the element with the specified value.
- `pop()` - This method removes the element at the specified index.
- `clear()` - This method removes all the elements from the list.

There are more methods! Check out the slides from class or online for more information.

## Your Lab

|Part | Topic |
| --- | --- |
|A | Sorted Lists|
|B | Same but Different Order? |
|C | Tic Tac Toe (Optional) |

### Part A ~ **Sorted Lists**
In this scenario, Cashier-Bot has become the CEO of **Cash's Burger Corp**. They are now in charge of flying to cities which are interested in creating new, franchised locations. Complete the function `sorted_cities that`, given a string with the names of cities separated by commas, prints a list of the cities in sorted order. This function returns `None`. Feel free to copy the code below, but **do not modify any of it.**

**Some Tips**


```python
# TODO: sorted_cities is given a string of city names separated by commas
# and prints out the names in sorted order. It returns None
def sorted_cities(city_names):
    pass
    

# Debugging function calls. You can add more or change
# The following should print Boston, Chicago Indianapolis
# and San Francisco in that order each city on a new line
sorted_cities('San Francisco,Boston,Chicago,Indianapolis')
```

### Part B ~ **Same but Different Order?**
In this scenario, Conversion-Bot, Cashier Bot's sister, has been promoted to the Vice President of **Cash's Burger Corp**. She are now in charge of the company's finances. Complete the function `same_but_different_order` that, given two lists of integers, returns `True` if the lists contain the same elements, but not necessarily in the same order. Otherwise, it should return `False`. Feel free to copy the code below, but **do not modify any of it.**

```python
# TODO: same_but_different_order is given two lists and returns True
# if lists contain the same elements, possibly in different orders,
# and False otherwise
def same_but_different_order(list1, list2):
    pass


# Below is our test code. Do not modify it, but you may add your own prints.
assert(same_but_different_order([1, 2, 3], [3, 1, 2]) == True) 
assert(same_but_different_order([1, 1, 1, 2],[1, 2, 1, 1]) == True)
assert(same_but_different_order([1, 2, 3, 1], [1, 2, 3]) == False)
assert(same_but_different_order([1, 1, 2, 3], [1, 3, 2, 2]) == False)
```

**About Assert**
- `assert()` is a function in Python that you can use to test your code. If the condition is `True`, the program will continue to run. If the condition is `False`, the program will stop and throw an error.


### Part C ~ Tic Tac Toe (Optional)

Using the following code, you will work towards implementing a tic tac toe game that uses lists of lists. You will create boards and check if player X or player O has won. Feel free to copy the code below.

```python
# TODO: Define variables for the characters on the board
x = 'X'
o = 'O'
empty = '_'

# This is an example of how to create a list of only empty spaces
empty_row = [empty, empty, empty]

# TODO: Complete the board so that it has three empty rows
# We have started off with a single empty row
board0 = [[empty, empty, empty]]

# TODO: Complete code that will create the following board
# We have provided code for the first of the three rows
# X _ O, _ X O, X _ _
board1 = [[x, empty, o]]

# TODO: Write code to create the following board
# X _ O, _ X O, O _ X
board2 = []

# TODO: Complete the function has_won that, given a board,
# will return True if and only if the Player X or O passed
# to it has won that board by filling a row, column, or
# diagonal. You may assume all boards are 3 by 3
# and all rows have same length
def has_won(board, player):
    pass

# Here is some testing code. You can create new boards
# to test for row and column wins
assert(has_won(board0, x) == False)
assert(has_won(board1, o) == False)
assert(has_won(board2, x) == True)
      
# TODO: For even more challenge if you are interested,
# can you use your board and has_won function
# to complete an implementation for a tic tac toe game?
# Start from an empty board and prompt players for moves
# until a player has won or the board is full
```