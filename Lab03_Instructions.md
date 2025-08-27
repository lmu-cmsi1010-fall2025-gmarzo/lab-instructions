# Welcome to Lab03 and Functions!

### Data Types

In this lab, you will use functions in Python.

## Notes 

### Functions

Functions are used to perform a specific task. They allow you to reuse code and make your code more readable.

Here is an example of a function in Python:
```python
def say_hello():
    print("Hello, World!")
```
> In this example, the function `say_hello` will print "Hello, World!" when called.

We can also pass parameters into our functions. Here is an example:
```python
def say_hello(name):
    print("Hello, " + name + "!")
```
> In this example, the function `say_hello` will take in a parameter `name` and print "Hello, {name}!" when called.

You can also return a value from a function. Here is an example:
```python
def add(x, y):
    return x + y
```
> In this example, the function `add` will take in two parameters `x` and `y` and return the sum of the two.

### Print Vs Return
When you use `print` in a function, the function will print the value to the console. When you use `return`, the function will return the value to the caller.

Here is an example:
```python
def add(x, y):
    print(x + y)
    return x + y
```

To then save the return value, set it to a variable:
```python
result = add(2, 3)
```

### Farenheit to Celsius
Here is a function that converts Farenheit to Celsius:
```python
def farenheit_to_celsius(farenheit):
    celsius = (farenheit - 32) * 5/9
    return celsius
```

## Your Lab

|Part | Topic |
| --- | --- |
|A | Temperature Conversion|
|B | Inches to Centimeters |
|C | Total Bill |



### Part A ~ Temperature Conversion
In this scenario, you will need to help program Cashier-Bot's baby sister, Conversion-Bot. For this part, you will write a function that converts Celsius to Farenheit for her programming. 

Above, there is a function that converts Farenheit to Celsius. Your task is to write a function that converts Celsius to Farenheit. Call this function `celsius_to_farenheit`.

After you have written the function, test it by calling it with a value of `0` and printing the result.

Tips:
- The formula to convert Celsius to Farenheit is `Celsius * 9/5 + 32`.
- Make sure to return the value.
- Don't forget about how to define a function and your indentation!




### Part B ~ Inches to Centimeters
In this scenario, Conversion-Bot has been hired by the Cheesecake Factory to help export their cheesecakes to Europe. They need a program that will convert the size of their cheesecakes from inches to centimeters. Write a function that converts inches to centimeters. Call this function `inches_to_centimeters`. It will take in a parameter `inches` and `return` the value in centimeters.

After you have written the function, test it by calling it with a value of `10` and printing the result.

Tips:
- There are `2.54` centimeters in a inch.
- Make sure to return the value.
- Don't forget about how to define a function and your indentation!

### Part C ~ Total Bill
In this scenario, Cashier-Bot's stint at the Cheesecake was only mildly successful. After getting his sister a job, he's decided to strike out on his own with a new venture, **Cash's Droid Burgers**!! He needs to have a program to calculate any bill that is given to him and add the tip percentage the customer gave him. 

Write a function that calculates the total bill for a meal. The function should take in the cost of the meal (`meal_cost`) and the tip percentage (`tip_percent`). The function should `return` the total bill. 

`meal_cost` is a float that represents the cost of the meal.

`tip_percent` is a float that represents the tip percentage.

The beginning of the function should look like this:
```python
def total_bill(meal_cost, tip_percent):
    pass
```
    





