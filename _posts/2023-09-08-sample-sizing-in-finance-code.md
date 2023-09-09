---
title: Code for the Problems in "Probability and Sample Size in Finance"
layout: post
post-image: "samplesizefinance.jpeg"
description:
tags:
- Probability 
- Sample Size 
---



```python
from math import comb

def probability(choose, num_items):
    return comb(num_items, choose) * (0.5)**choose * (1-0.5)**(num_items-choose)

def total_probability(choices, num_items):
    print("Num Items", num_items)
    value = 0
    for choose in choices:
        current = probability(choose, num_items)
        print(choose, " ", current)
        value = value + current
    print("Total ", value, "\n")


total_probability(range(0, 5), 10)

total_probability(range(0, 4), 12)

total_probability(range(0, 6), 20)  
```

Output

```
Num Items 10
0   0.0009765625
1   0.009765625
2   0.0439453125
3   0.1171875
4   0.205078125
Total  0.376953125 

Num Items 12
0   0.000244140625
1   0.0029296875
2   0.01611328125
3   0.0537109375
Total  0.072998046875 

Num Items 20
0   9.5367431640625e-07
1   1.9073486328125e-05
2   0.0001811981201171875
3   0.001087188720703125
4   0.004620552062988281
5   0.0147857666015625
Total  0.020694732666015625 

```