# Welcome to Lab07 and Exam 1 Review!

### Exam 1 Review (Optional)

In this lab, you will review the topics that will be covered on Exam 1.

These topics are:
- Variables
- Data Types
- Operators
- Functions
- Conditionals
- Loops
- Lists
- Strings

## Notes 



## Your Lab

|Part | Topic |
| --- | --- |
|A | and & or |
|B | Coupons! |


## Part A ~ **and & or**
In this part, you will be creating two functions that will replace the `and` and `or` operators. First, let's review what `and` and `or` do.

```python
# Quick review of `and` and `or` (as well as types and loops!).
for left_boolean in (True, False):
    for right_boolean in (True, False):
        print(left_boolean, 'and', right_boolean, '==',
              left_boolean and right_boolean)

print() # Blank line for spacing.

for left_boolean in (True, False):
    for right_boolean in (True, False):
        print(left_boolean, 'or', right_boolean, '==',
              left_boolean or right_boolean)
```

Feel free to run this code on your own to see what it does. However, you **do not need to submit this code**. Running the above code will show you the truth tables for `and` and `or`. Use this information to create two functions: `my_and` and `my_or`.

```python
def my_and(left, right):
    pass

def my_or(left, right):
    pass
```

These functions should return the same results as the `and` and `or` operators. For example, `my_and(True, False)` should return `False` and `my_or(True, False)` should return `True`.

Once you complete the two functions, it is now time to test it. You can use the following code to test your functions:

```python
for left_boolean in (True, False):
    for right_boolean in (True, False):
        print(left_boolean, 'and', right_boolean, '==',
              my_and(left_boolean, right_boolean))

print() # Blank line for spacing.

for left_boolean in (True, False):
    for right_boolean in (True, False):
        print(left_boolean, 'or', right_boolean, '==',
              my_or(left_boolean, right_boolean))
```

This code should print out the exact same truth tables as the first code snippet. If it does, then you have successfully completed both functions.

### Part B ~ **Coupons!**

In this part, you will be creating a program that will collect 10 unique coupons. These coupons will be represented by the numbers 1 through 10. Using the started code below, **finish the program to continue getting coupons until you collect all 10, unique coupons**. Use the `get_coupon` function to get coupons. Keep track of the total number of coupons you collect before you collect each distinct coupon in the set of 10. Remember you can get any of the 10 coupons at any time so you may get many coupons several times before you get all 10.

```python
import random

# This function simulates getting a coupon from a set of 10 coupons. 
def get_coupon():
    coupon = random.randint(1, 10)
    return coupon

# Below, keep on collecting coupons until you get all 10 coupons.

# Use this list to store the coupons you have collected.
coupon_collection = [] 
# Use this variable to store the total number of coupons you have received.
coupons_received = 0

# TODO: Keep on receiving coupons until you have collected the whole set.
# This is what you would do for a single coupon:
coupon = get_coupon()
coupons_received = coupons_received + 1
if coupon not in coupon_collection:
    coupon_collection.append(coupon)

# Print out your coupon collection.
print(coupon_collection)

# Print out the total number of coupons received.
print('Number of coupons received:', coupons_received)

assert(sorted(coupon_collection) == list(range(1, 11)))
```