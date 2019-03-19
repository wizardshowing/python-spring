# Assignment 7 - Matplotlib

## About Matplotlib

Matplotlib is a library that allows you to make (beautiful) graphs and figures in Python.

## First

Before working on this assignment, read the following:

- [Tutorial how to use Matplotlib](https://www.datacamp.com/community/tutorials/matplotlib-tutorial-python)
- [Another tutorial (more advanced)](https://github.com/rougier/matplotlib-tutorial#bar-plots)
- [Matplotlib gallery](https://matplotlib.org/gallery.html), to get inspiration

## Glassdoor.com

[Glassdoor](www.glassdoor.com) is a website where employees can leave reviews (anonymously). For example, reviews for EY can be found at [https://www.glassdoor.com/Reviews/EY-Reviews-E2784.htm](https://www.glassdoor.com/Reviews/EY-Reviews-E2784.htm)

## Required

For this assignment it is required to impress me :). Use [this Glasdoor.com dataset](datasets/glassdoor.csv) to create interesting/usefull visualizations with Matplotlib.

> Link to dataset in raw format (to copy/paste): [https://raw.githubusercontent.com/JoostImpink/python-spring/master/assignments/datasets/glassdoor.csv](https://raw.githubusercontent.com/JoostImpink/python-spring/master/assignments/datasets/glassdoor.csv)

## Glassdoor dataset

The dataset consists of 438 ratings for employees of Florida offices of the 8 largest Audit firms. Reviews were downloaded summer 2017. 

Most of the variables are self-explanatory. Rating variables are between 1 (lowest) and 5 (highest).

Rating variables:

- overall_rating: Overal rating
- worklife: Rating for work-life balance
- cultule_values: Rating for culture/values
- career: Rating for career
- compensation: Rating for compensation
- seniormanagement: Rating for senior management

## Sample code

The following code will read the firm name, work-life balance and culture into lists:

```python
# assumes that glassdoor.csv is in the same folder
with open('glassdoor.csv') as f:
    content = f.readlines()

# empty lists (to hold the values)
company = []
worklife = []
culture = []
# [1:] means skip the first line (header)
for line in content[1:]:
    # split each line into a list of items 
    items = line.split(',')
    # company name is the 5th column (so index is 4)
    company.append( items[4] )
    worklife.append (float( items[5] ) )
    # culture is sometimes missing (float doesn't work on a missing)
    # first get it as a string
    cul = items[6];
    # if 'not' (i.e. missing), set it to "0"
    if (not cul):
        cul = "0"
    # now it is either "0" or some number (as text)
    culture.append ( float(cul) ) 
    
print('company', company, 'work life balance', worklife, 'culture', culture)  
```
