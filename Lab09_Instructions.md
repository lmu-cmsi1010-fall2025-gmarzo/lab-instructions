# Welcome to Lab09 and Dictionaries!

### Dictionary

In this lab, you will use dictionaries in Python.

## Notes 

### Dictionaries


## Your Lab

|Part | Topic |
| --- | --- |
|A | Getting Words from Strings|
|B | Find that Frequency! |
|C | Similarity Scores|

### Part A ~ Getting Words from Strings

In this scenario, Cashier-Bot needs to reset their english chip on the language processor. To do this, they need to process a string and get all the words from it. Using the strings below, write a program that will take the strings and put them into a list. For all of the strings, you will need to save the words in a *separate* list of strings.

```python
# credit for the qutoes goes to: https://oxfordsummercourses.com/articles/books-for-english-literature-students-to-read/ and the authors as well
fitzgerald_quote = """in my younger and more vulnerable years my father gave me some advice that I’ve been turning over in my mind ever since whenever you feel like criticizing any one he told me just remember that all the people in this world haven’t had the advantages that you’ve had"""
dickens_quote = """suffering has been stronger than all other teaching and has taught me to understand what your heart used to be I have been bent and broken but I hope into a better shape"""
lee_quote = """you never really understand a person until you consider things from his point of view until you climb inside of his skin and walk around in it"""
austen_quote = """nobody who has not been in the interior of a family can say what the difficulties of any individual of that family may be"""


# TODO: Edit the 4 lines of code to save the words from each quote to use for the rest
# of the lab. Be sure to save the words for each quote in a list of strings.
fitzgerald_words = []
dickens_words = []
lee_words = []
austen_words = []

# Our test code is below. Do not modify it.
assert(len(fitzgerald_words) == 49)
assert(len(dickens_words) == 33)
assert(len(lee_words) == 27)
assert(len(austen_words) == 24)
```

**Some Tips**
- You can use a string method here to split the string into a list of words.
- We aren't using a dictionary just yet! We're just getting ourselves set up.

### Part B ~ Find that Frequency!

Now that Cashier-Bot has all the words loaded into their english chip, they need to find the frequency of each word in the quotes. Using the words you saved from the previous part, write a function called `frequency` that will count the frequency of each word in the quotes. You will need to save the frequency of each word in a dictionary. Then finally, `return` the dictionary.

```python
def frequency(words):
    word_counts = {}

    return word_counts



# TODO: frequency is given a list of words
# and returns a dictionary of the counts of each
# word in the list of words
def frequency(words):
    # Empty dictionary that will be filled and returned
    word_counts = {}

    # TODO: Loop through each word in the words list
    # if the word is in the dictionary, increment its count
    # otherwise, add the word to the dictionary and set its
    # count to 1

    return word_counts


# Call the frequency function to get the word counts dictionary
# for each quote above
fitzgerald_counts = frequency(fitzgerald_words)
dickens_counts = frequency(dickens_words)

# TODO: Call the frequency function to get the word counts for the Lee
# and Austen quotes
lee_counts = {}
austen_counts = {}

assert(len(fitzgerald_counts) == 40)
assert(len(dickens_counts) == 28)
assert(len(lee_counts) == 22)
assert(len(austen_counts) == 20)
assert(fitzgerald_counts['my'] == 3)
assert(dickens_counts['and'] == 2)
assert(lee_counts['you'] == 3)
assert(austen_counts['a'] == 1)

```

**Some Tips**
- You can use a dictionary to keep track of the counts of each word.
- You can use a loop to go through each word in the list of words.
- You can use the `in` operator to check if a key is in the dictionary.

### Part C ~ Similarity Scores
Finally, Cashier-Bot's english chip reset is almost complete! All Cashier-Bot needs is to compute the similarity score btween two different dictionaries. Write a function `similarity_score` that takes in *two* dictionaries and returns the similarity score. The similarity score is **between 0 and 1** where 1 indicates that the strings are identical and 0 indicates that they have no words in common.

```python
# TODO: Complete this function similarity_score
# Given the dictionaries for counts for two lists of words,
# similarity_score will return a score between [0, 1] with 1
# being identical and 0 no words in common.
# The similarity score is 
# 1-((number of different words in the string)/(total number of words in both strings))
# We explain how to calculate this in comments
def similarity_score(words1_counts, words2_counts):
    # TODO: Calculate the total number of words in both frequency dictionaries
    total = 0

    # Let's calculate the difference in the number of words in each
    # word counts. This variable is used to keep track of the difference
    # as we go through each word counts
    difference = 0

    # Calculate how many words are in words1 but not in words2
  
    # TODO: Translate the following pseudo-code into code:
    # Loop through words1_counts
        # If the word is also in words2_counts
            # Count how many more times word is in words1 than words2 or vice versa
            # if they have the same in both this should be zero
            # add the difference to the running difference variable.
        # Otherwise:
            # this word is in words1 but not in words2 at all,  
            # so add frequency in words1 to the difference variable
      

    # Calculate how many words are in words2 but not in words1
    # We have already checked for words that are in words1, so we
    # only need to worry about words in words2 but not in words1
  
    # TODO: Translate the following pseudo-code into code:
    # Loop through words in words2_count
        # If it is not in words1 also:
            # add the frequency in words2 to the difference
   

    # TODO: Calculate the similarity score: 1 is if words1 and words2 were identical
    # and 0 if no words in common. Subtract from 1 the 
    # difference in words calculated above divided by the total number of words.
    similarity = 1.0 

    return similarity


# Here we are calling the similarity function to see the 
# similarity between the quotes. You do not need to change this code.
# Hint: The quotes are not very similar. You may add some other quotes
# that you write that are more similar to get higher similarity scores.
# Remember that the highest similarity score should be 1 and the lowest 0.
# Until you implement the similarity score function these will all have
# similarity score 1

print("The similarity between the Dickens and Fitzgerald quote: ",\
      similarity_score(fitzgerald_counts, dickens_counts))
print("The similarity between the Lee and Fitzgerald quote: ",\
      similarity_score(fitzgerald_counts, lee_counts))
print("The similarity between the Austen and Fitzgerald quote: ",\
      similarity_score(fitzgerald_counts, austen_counts))
print("The similarity between the Austen and Lee quote: ",\
      similarity_score(lee_counts, austen_counts))
print("The similarity between the Austen and Dickens quote: ",\
      similarity_score(dickens_counts, austen_counts))
print("The similarity between the Lee and Dickens quote: ",\
      similarity_score(dickens_counts, lee_counts))

assert(0.18 > similarity_score(dickens_counts, austen_counts) > 
       similarity_score(fitzgerald_counts, austen_counts) > 
       similarity_score(lee_counts, austen_counts) > 
       similarity_score(dickens_counts, lee_counts) > 
       similarity_score(fitzgerald_counts, dickens_counts) > 
       similarity_score(fitzgerald_counts, lee_counts) > 0)
```

**Some Tips**
- Follow along closely with the comments in the code
- You will need to use loops, dictionaries, and variables to keep track of the counts of words.
- You will need to calculate the similarity score using the formula provided.
