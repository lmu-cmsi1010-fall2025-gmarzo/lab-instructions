# Welcome to Lab05 and Strings!

### Strings

In this lab, you will use loops in Python.

## Notes 

### Strings
Strings are used in Python to record text information, such as names. For example, Python understands the string "hello" to be a sequence of letters in a specific order. This means we will be able to use indexing to grab particular letters (like the first letter, or the last letter).

### Indexing
Indexing allows you to grab a single character from a string. Indexing starts at 0. Here is an example:
```python
my_string = "Hello, World!"
print(my_string[0])
```
> In this example, the code block `print(my_string[0])` will print "H".

### Slicing
Slicing allows you to grab a subsection of a string. Here is an example:
```python
my_string = "Hello, World!"
print(my_string[0:5])
```
> In this example, the code block `print(my_string[0:5])` will print "Hello".

### String Methods
There are many, different methods for strings in Python. Here are a few:
- `upper()` - This method returns the string in uppercase.
- `lower()` - This method returns the string in lowercase.
- `replace()` - This method replaces a string with another string.
- `split()` - This method splits the string into a list.


## Your Lab

|Part | Topic |
| --- | --- |
|A | Character Counts-er |
|B | Work Repeater |
|C | Name Mixer |



### Part A ~ Character Counts-er
In this scenario, Cashier-Bot's restaurant, **Cash's Droid Burgers**, has grown like crazy, spawning multiple franchised locations!

Write a function that count how often a given letter appears in the word. The function should take in two parameters: two strings `word` and `letter`. The function should `return` and integer which is the number of times the letter appears in the string.

>If you put in the string `"hello"` and the letter `"l"`, the function should return `2`.

**Some Tips**
- You can use a loop to go through each character in the string.
- Make sure you're taking in 2 parameters: the word and the letter.


**Test Cases**

Test your function with the following test cases:
| Word | Letter | Expected Output |
| --- | --- | --- |
| `banana` | `a` | `3` |
| `hello` | `l` | `2` |
| `world` | `d` | `1` |

Feel free to add more test cases to make sure your function works as expected.

### Part B ~ Work Repeater
In this scenario, Cashier-Bot has been working so hard at **Cash's Droid Burgers** that they've been repeating themself! Write a function that takes in a string and a number, and returns the string repeated that many times.

>If you put in the string `"hello"` and the number `3`, the function should return `"hellohellohello"`.

**Some Tips**
- Don't forget that some arithmetic operators can be used on strings. 

**Test Cases**

Test your function with the following test cases:
| Word | Number | Expected Output |
| --- | --- | --- |
| `hello` | `3` | `hellohellohello` |
| `hi` | `2` | `hihi` |
| `potato` | `4` | `potatopotatopotatopotato` |

### Part C ~ Name Mixer
In this scenario, Cashier-Bot is still mixing themself up! Now they'll hear names and swap them around. Write a program that takes in two names, swaps their first names, and returns the new names.

>If you put in the names `"Cashier Bot"` and `"Jason Douglas"`, the program should return `"Jason Bot"` and `"Cashier Douglas"`.

**Some Tips**
- Check out your string methods! You can use them to split the names into lists, and then recombine them.

**Test Cases**

Test your program with the following test cases:
| Name 1 | Name 2 | Expected Output |
| --- | --- | --- |
| `Cashier Bot` | `Jason Douglas` | `Jason Bot` and `Cashier Douglas` |
| `John Doe` | `Jane Smith` | `Jane Doe` and `John Smith` |
| `Bob Ross` | `Spongebob Squarepants` | `Spongebob Ross` and `Bob Squarepants` |