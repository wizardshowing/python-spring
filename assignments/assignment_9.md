# Assignment 9 - Benford's Law


## First

Before working on this assignment, read the following:

- [Benfords Law.pdf](https://www.agacgfm.org/aga/fraudtoolkit/documents/benfordslaw.pdf)

## Required

You are responsible for the audit of a company. One of the subsidiaries has provided you weekly sales data. You suspect the manager of this subsidiary may have cooked the books (i.e., the sales numbers provided are incorrect).

Use Benford's Law to detect potential fraud in the numbers provided.

## Data

Copy/paste the following lines in a new file and call this file `salesdata.txt`:

```
17900
66100
11300
94600
10600
28700
37800
69600
11100
38300
16400
55500
50800
18100
89000
31900
88500
13600
30300
19800
37900
94200
20500
54100
10900
33900
35000
52700
18300
20500
18100
94100
62700
30300
21000
31900
40600
28000
34600
42800
98400
16800
14800
64000
81200
50900
33300
25700
21600
25500
65800
20800
32600
82000
32500
52700
26600
13000
52300
59800
21700
95300
15000
18500
83600
56200
11500
51100
45500
93500
14000
51000
13500
47200
71300
80500
90600
65000
94100
73200
22900
44700
47500
72400
53000
75300
10200
69100
18800
13300
19300
37000
55500
13000
54600
11800
40900
34800
58000
```

## Note

The following function returns the most significant digit of a number

```python
def mostSig(x):
	# turn number to string, and take the first character, then transform back to integer
	return int(str(x)[0]) 
```

The following code generates the expected frequency of each leading digit as per Benford's law:

```python
benford = [log10(1 + 1/i) for i in range(1, 10)]
#benford` will hold a list:
[0.3010299956639812,
 0.17609125905568124,
 0.12493873660829993,
 0.09691001300805642,
 0.07918124604762482,
 0.06694678963061322,
 0.05799194697768673,
 0.05115252244738129,
 0.04575749056067514]
```

Meaning, the number 1 naturally occurs 30.1% of the time as the most significant digit; the number 2 17.6% of the time, etc.

### Calculations

See page 25 of the pdf (https://www.agacgfm.org/aga/fraudtoolkit/documents/benfordslaw.pdf) for the formulas to compute the standard deviation, and the z-value (formulas 2 and 3).
You may use 1.96 as the critical z-value. That is, for each of the digits 1-9, you compare the z-value for that digit with the critical z-value. When a z-value exceeds the critical value, this would indicate that the data is non-random (fraudulent).
