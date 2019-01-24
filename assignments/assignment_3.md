# Assignment 3: Files

This assignment is about processing data that is in a file.

# Tutorials to review

Make sure you have reviewed the following topics before starting to work on this assignment. 

Files: [https://www.py4e.com/lessons/files](https://www.py4e.com/lessons/files)


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
fhand = open('myInputFile.txt')
count = 0
for line in fhand:
    # do something
    count = count + 1
    print ('line ', count, line)
        
print('There were', count, 'lines in the file')
```

> Note: Review the string functions if needed. Remember to convert string to number before doing any calculations. Notice that each line ends with a newline.
