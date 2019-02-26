# Assignment 8 - Reciprocal method


## First

Before working on this assignment, read the following:

- [numpy tutorial](http://cs231n.github.io/python-numpy-tutorial/)
- [Solving a system of equations](https://medium.com/@GalarnykMichael/solving-system-of-linear-equations-using-python-645ad1904cec)


## Required

The following information is available for service departments S1 and S2:

- The costs of S1 are its own direct department costs of $10,000, and 15% of S2 total costs
- The direct department costs for S2 are $18,000; S2 uses 10% of the cost drivers of S1

Use numpy to compute the total department costs for S1 and S2 (using the reciprocal method), that is, what is the sum of the direct department costs plus the allocated department costs for S1 and S2?


## Note

Note this example to solve a system of equations using numpy:

```python
import numpy as np

# Solving following system of linear equation
# 1a + 1b = 35
# 2a + 4b = 94

a = np.array([[1, 1],[2,4]])
b = np.array([35, 94])

print(np.linalg.solve(a,b))
```