# Welcome to Lab12, Classes, and Objects!

### Class and Objects
In this lab, you will practice creating classes and objects in Python. 

## Notes

### What is a class?
A class is a blueprint for creating objects. It defines the properties and behaviors of objects. A class can be used to create almost anything you can think of.

Dogs! Cats! Cars! People! All of these can be represented as classes in Python.

### How to create a class?

To create a class in Python, you use the `class` keyword followed by the name of the class. Here is an example of a simple class:

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

In this example, we have created a class called `Dog` with two properties: `name` and `age`. We have also defined a special method called `__init__` which is the constructor method. The constructor method is called when an object of the class is created.

### What is an object?
An object is an instance of a class. It is a concrete entity based on a class and is created using the constructor method of the class.

Here is an example of creating an object of the `Dog` class from above:

```python
indy = Dog("Indy", 1)
panda = Dog("Panda", 8)
```

In this example, we have created two objects `indy` and `panda` of the `Dog` class. Each object has it's own properties, but they share the same behavior defined in the class.

### What is a method?

A method is a function that is associated with a class. It defines the behavior of the objects that are created from the class. Methods are defined inside the class and can be called on objects of the class.

Here is an example of a method in the `Dog` class:

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print("Woof! Woof!")
```

Then if you create an object of the `Dog` class, you can call the `bark` method on that object:

```python
indy = Dog("Indy", 1)
indy.bark()
```

## Your Lab

|Part | Topic |
| --- | --- |
|A | Go on a Walk!|
|B | Create an Owner Class|
|C | Complex Numbers|

### Part A ~ **Go on a Walk!**
Included is the code for the `Dog` class from the slides. Your task is to complete the `exercise` method. The `exercise` method should take an amount and decrease the dog's weight by that amount. Modify the code where the todo is!

```python
class Dog():
    """The Dog has a name, weight, and breed. It can eat or exercise."""
     
    # Constructor as given in slides
    def __init__(self, name, weight, breed):
        self.name = name
        self.weight = weight
        self.breed = breed

    # Method for the dog to eat given in slides
    # Notice that the weight of the dog increases
    # by the amount fed    
    def eat(self, amount):
        self.weight += amount

    # Write a method called exercise
    # that takes an amount and decreases the
    # dog's weight by that amount
    # TODO: ADD METHOD EXERCISE BELOW

toto = Dog('Toto', 13, 'Cairn Terrier')

assert(toto.name == 'Toto')
assert(toto.weight == 13)
assert(toto.breed == 'Cairn Terrier')
```


### Part B ~ **Create an Owner Class**
You will **complete the constructor for the Person class for dog owners**. Each person has a `name`, a `dog`, and a `generosity` level. The generosity level is a value between 0 and 1 (inclusive) that is the amount of a pound of food that owners feed their dogs. You will also **complete the feed_dog method for the Person**. This method will feed the owners' dogs the amount of their generosity. 
```python
class Person(object):
    """The Person has a name, a Dog, and a generosity. It can feed its Dog."""

    # TODO: Complete the constructor the the Person below
    # Be sure to save each input parameter except
    # self as an attribute
    def __init__(self, name, dog, generosity):
        pass

    # TODO: Complete the following feed_dog method
    # The amount of food that people
    # feed their dogs are their generosity 
    def feed_dog(self):
        pass
```

Finally, use the following code to test your implementation! Make sure to fill in the todos!
```python
# Create a Person object with name Gregory
# Gregory owns a Border Terrier named Hickory, whose weight is 15.2 pounds.
# Gregory's generosity is 0.1.
#
#  - The dog parameter for creating the Person object for Gregory
#    will be the Dog object that is created for Hickory.
#
#  - The generosity is a floating point number such that 0 ≤ generosity ≤ 1
#

# TODO: Instantiate the owner and dog objects!
dog = None
owner = None

print(owner.name + ' owns a ' + owner.dog.breed + ' named ' + owner.dog.name)
print(owner.dog.name + ' weighs ' + format(owner.dog.weight, 'f') + ' lbs.')
# Should be 'Gregory owns a Border Terrier named Hickory'
#           'Hickory weighs 15.200000 lbs.'

# Gregory feeds Hickory.
# TODO: Make Gregory feed Hickory.
print('After eating ' + owner.dog.name + ' weighs ' \
      + format(owner.dog.weight,'f') + ' lbs.')
# Should be 'After eating Hickory weighs 15.300000 lbs.'

assert(owner.name == 'Gregory')
assert(owner.generosity == 0.1)
assert(owner.dog == dog)
assert(dog.name == 'Hickory')
assert(dog.breed == 'Border Terrier')
assert(round(dog.weight, 2) == 15.3)
```

### Part C ~ **Complex Numbers**
Complex numbers have a real part and an imaginary part. The imaginary part is multiplied by i, the square root of -1. A complex number can be written a + bi where a is the real part and b is the imaginary part. Copy the following code and complete the todos!

```python
class Complex(object):
    """A complex number has a real and imaginary part."""

    # TODO: Complete the constructor; save each input parameter except
    # self as an attribute
    def __init__(self, real, imaginary):
        pass

    # TODO: Complete the method real to return the real part of
    # of the Complex number
    def real_part(self):
        pass

    # TODO: Complete the method imaginary to return the imaginary part of
    # of the Complex number
    def imaginary_part(self):
        pass

    # TODO: Complete the method add to the calling complex number
    # to the argument complex number and RETURN A NEW COMPLEX
    # NUMBER THAT IS THEIR SUM, i.e., add the real parts to get the
    # new real, and add the imaginary parts to get the new imaginary
    def add(self, other):
        pass

    # This method is given to you to turn a Complex object
    # into a string. Please do not change this function.
    # It permits you to print a Complex number in the format
    # a + bi where a is the real part and b is the imaginary part.
    def __str__(self):
        output = str(self.real) + ' + ' + str(self.imaginary) + 'i'
        return output


# Feel free to add to this code in order to test your implementation further.
x = Complex(3, 4)
print('x is ' + str(x)) # Should print 3 + 4i
assert(x.real == 3)
assert(x.imaginary == 4)

y = Complex(7, 10)
print('y is ' + str(y)) # Should print 7 + 10i
assert(y.real == 7)
assert(y.imaginary == 10)

sum = x.add(y)
print('sum is ' + str(sum)) # Should print 10 + 14i
assert(sum.real == 10)
assert(sum.imaginary == 14)
```