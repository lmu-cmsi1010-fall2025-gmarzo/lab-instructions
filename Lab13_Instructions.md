# Welcome to Lab 13 and Inheritance! 

### Inheritance

In this lab, you will practice using inheritance in Python. Make sure to read everything thoroughly and send me a message if you have any questions!

## Notes

### What is inheritance?
Inheritance is a way to create a new class that is based on an existing class. The new class inherits the attributes and methods of the existing class, and can also have its own attributes and methods.

### How to use inheritance?
To create a new class that inherits from an existing class, you use the following syntax:

```python
class NewClass(ExistingClass):
    # class definition
```

In this example, `NewClass` is the new class that is being created, and `ExistingClass` is the existing class that `NewClass` is inheriting from.

Whatever class you want to inherit from should be in the parentheses after the class name. Sometimes you'll see `object` in the parentheses, which is the default class that all classes inherit from. Think of it as the Mew of classes or that fish that decided to grow legs one day. (this is a simplication of evolution pls don't take it as a scientific fact)

### What is a superclass and subclass?
The existing class that is being inherited from is called the **superclass**, and the new class that is inheriting from the superclass is called the **subclass**.

### What is the `super()` function?
You may see the `super()` function being used in the constructor method of a subclass. The `super()` function is used to call the constructor method of the superclass.

When you use the `super()` function, you can access the attributes and methods of the superclass in the subclass. This allows us to reuse code and avoid making our class creations too complex.

Here is an example of using the `super()` function in a subclass:

```python
class Dog:
    def __init__(self, name):
        self.name = name

class Labrador(Dog):
    def __init__(self, name, color):
        super().__init__(name)
        self.color = color
```


## Your Lab
|Part | Topic |
|---|---|
| A | Rock, Paper, Scissors... with Classes! |
| B | Ready Player One! |
| C | RPC Showdown! |

### Part A ~ **Rock, Paper, Scissors... with Classes!**

For this part, we're going to revist Rock, Paper, Scissors, but this time we're going to use classes! Don't worry, we aren't going as in-depth as we did either.

In this lab, we're going to give you some starter code for you all to finish. For this first part, we've given you a parent class called `Strategy` and a subclass called `RockStrategy`. For this part, **you will need to complete the `PaperStrategy` and `ScissorsStrategy` classes**.

```python
# This is the parent class for all possible strategies
class Strategy():
    # The constructor initializes the strategy description
    def __init__(self, desc):
        self.__description = desc

    # This method is used to describe what a strategy does      
    def use(self):
        return 'uses a generic strategy'
    
    # This method the name of the strategy class
    def get_id(self):
        return self.__class__.__name__

    # This method is used to print a strategy and does not need to be
    # changed
    def __str__(self):
        return self.__description
    
    # This method is use to describe what will happen when two
    # strategies are played against each other. This returns one
    # of three values:
    # 
    # * Return -1 if other beats self
    # * Return 1 if self beats other
    # * Return 0 if it's a tie
    # 
    def fight(self, other):
        return 0


# We have completed the RockStrategy class for you. Its parent is the
# Strategy class. It overrides use() and fight() and uses its parent
# constructor, get_id(), and __str__() 
class RockStrategy(Strategy):
    def __init__(self):
        super().__init__('Playing the rock')
            
    def use(self):
        return 'Rock!!'
    
    def fight(self, other):
        if other.get_id() == 'RockStrategy':
            print('Tie')
            return 0
        elif other.get_id() == 'PaperStrategy':
            print('Paper wins over rock')
            return -1
        elif other.get_id() == 'ScissorsStrategy':
            print('Rock wins over scissors')
            return 1


# TODO: Now you will complete the Paper and Scissors Strategy classes below.
class PaperStrategy(Strategy):
    pass


class ScissorsStrategy(Strategy):
    pass

# The following code tests your code. Do not change it.
rock_strategy = RockStrategy()
scissors_strategy = ScissorsStrategy()
paper_strategy = PaperStrategy()

assert(rock_strategy.fight(rock_strategy) == 0)
assert(scissors_strategy.fight(scissors_strategy) == 0)
assert(scissors_strategy.fight(scissors_strategy) == 0)
assert(rock_strategy.fight(scissors_strategy) == 1)
assert(rock_strategy.fight(paper_strategy) == -1)
assert(scissors_strategy.fight(paper_strategy) == 1)
```

### Part B ~ **Ready Player One!**
For part B, we're going to finish the Player class. We have our generic Player class and a ComputerPlayer class that plays a random strategy. **You will need to complete the HumanPlayer class**. Follow the instructions in the comments to complete the class.

```python
import random

# This is the parent class for all players. 
class Player():
    # The constructor initializes the strategy description
    def __init__(self, name):
        self.name = name

        # Every player has all the strategies for the game in a dictionary
        # The keys are the names of the strategies, and the values are 
        # instances of the corresponding strategy objects.
        self.strategies = {
            'rock': RockStrategy(),
            'paper': PaperStrategy(),
            'scissors': ScissorsStrategy()
        }

        self.score = 0
  
    def __str__(self):
        return 'Player: ' + self.name
    
    # This method should return a strategy for the player, but does nothing yet;
    # the derived classes will override it.
    def play_strategy(self):
        return 0
    
    def update_score(self, own, other):
        print(f'{self.name} says: "{own.use()}"')
        self.score += own.fight(other)
    
    def get_score(self):
      return self.score


# We have completed the Computer Player for you.
# The Computer Player plays a random strategy of rock, paper, or scissors.    
class ComputerPlayer(Player):
    def __init__(self, name='Computer Player'):
        super().__init__(name)

    def play_strategy(self):
        strategy = random.randint(1, 3)
        if strategy == 1:
            return self.strategies['rock']
        elif strategy == 2:
            return self.strategies['paper']
        else: # 3 is only value left
            return self.strategies['scissors']


# TODO: Now you will complete the HumanPlayer.
#
# The main override here is that the play_strategy() method should
# prompt the human user for a strategy--input is valid if it is
# a key in the strategies dictionary. (note the key is lowercase!)
class HumanPlayer(Player):
    pass
```

### Part C ~ **RPC Showdown!**
For this last part, you don't need to implement anything! We've given you the code to run a game of Rock, Paper, Scissors. Add this at the bottom of your lab and try it out!

```python
# Instantiating a computer player
walle = ComputerPlayer()

# Instantiating a human player
human_name = input('Please enter your name, human player: ')
human_player = HumanPlayer(human_name)

for i in range(5):
    computer_strategy = walle.play_strategy()
    human_strategy = human_player.play_strategy()

    print()
    print(str(walle)+ ' ' + str(computer_strategy))
    print(str(human_player)+ ' ' + str(human_strategy))
    print()

    walle.update_score(computer_strategy, human_strategy)
    human_player.update_score(human_strategy, computer_strategy)

    print()
    print(str(walle)+ "'s score: " + str(walle.get_score()))
    print(str(human_player)+ "'s score: " + str(human_player.get_score()))
    print()

walle_score = walle.get_score()
human_score = human_player.get_score()

if walle_score == human_score:
    print('Good match: Tie')
elif walle_score > human_score:
    print('Computer wins!')
else:
    print('You win!')
```