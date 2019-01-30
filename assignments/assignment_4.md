# Assignment 4


# Tutorials to review

Make sure you have reviewed the following topics before starting to work on this assignment.

Dictionaries: [https://www.py4e.com/lessons/dictionary](https://www.py4e.com/lessons/dictionary)

# Description

Use the same file as used in assignment 3, but instead of creating several variables (for sales in units, price, fixed costs, etc) instead store these as key-value pairs on a dictionary.

So, after processing the file, the dictionary will have the following key-value pairs:

- key 'salesUnits' with value 500
- key 'priceUnit' with value 11
- key 'fixedCosts' with value 2500
- key 'variableCostUnit' with value 2

There is no need to compute the break-even point. Include code that prints each of the keys (salesUnits, etc) in uppercase.

## Starting point

```python
# read the lines of the file into a list
with open('myInputFile.txt') as f:
    content = f.readlines()

# new dictionary
myDict = {} 
print('empty dictionary', myDict)

# go through the lines of the file
for line in content:
    # this code runs for each element in the list (content is a list)
    print ('dictionary is now', myDict)
    # you will need to add code here that processes the line
    # that is, taking the value (after the colon) and turning it into a number
    # and setting a key-value property on 
    # todo
       
# all done, print dictionary
print(myDict) 
# include the code that prints all the keys in uppercase
# todo
```