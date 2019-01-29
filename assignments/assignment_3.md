# Assignment 3: Files

This assignment is about processing data that is in a file.

# Tutorials to review

Make sure you have reviewed the following topics before starting to work on this assignment. 

Files: [https://www.py4e.com/lessons/files](https://www.py4e.com/lessons/files)

Lists: [https://www.py4e.com/lessons/lists](https://www.py4e.com/lessons/lists)

## Input file

Copy/paste the following lines in a new file and call this file `myInputFile.txt`:

```
salesUnits:500
priceUnit:11
fixedCosts:2500
variableCostUnit:2
```

Make sure that the file is saved in the same folder that you are using for Jupyter Notebook. To find out in which folder your Jupyter notebook is, run the following code:

```
import os
cwd = os.getcwd()
print(cwd)
```

## Assignment

Create a program that reads the input file, assigns the values to relevant variables that are then used to compute (and print) the break-even point (in units).

Please submit your python code along with the output of the program.

## Similar code (to adapt from)

You can adapt the following code to assign the values to corresponding variable names (like `salesUnits`, `priceUnit`):

```python
# read the lines of the file into a list
with open('myInputFile.txt') as f:
    content = f.readlines()


print('variable content is of type', type(content))

# count variable (will increase it by 1 for each line)
count = 0
print('print content')
for line in content:
    # this code runs for each element in the list (content is a list)
    count = count + 1
    print ('line ', count, line)
    # you will need to add code here that processes the line
    # that is, taking the value (after the colon) and turning it into a number
    # and setting the right variable
        
# this will run once all elements in content are printed 
print('There were', count, 'lines in the file')
# here you would do the break-even calculation with the variables read from the file
# that is, you should have a variable that has the units sold set to 500,
# the price per unit being 11 etc 
```

> Note: Review the string functions if needed. Remember to convert string to number before doing any calculations. Notice that each line ends with a newline.
