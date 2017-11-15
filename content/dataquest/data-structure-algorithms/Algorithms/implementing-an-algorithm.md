+++
title = "Implementing an Algorithm"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T18:19:39-05:00
categories = ["dataquest"]
weight = 4002
draft = false
+++

Let's start with a simple algorithm that searches for a value in a list. We could use a linear search algorithm to do this. Remember that an algorithm is a particular method for performing a task, and linear search is only one of several algorithms that can solve this problem.

Linear search checks a list of items for a particular value by reviewing each item in the list until it finds the one it's looking for. If it doesn't find a matching item, we can conclude that there's no matching item in the list.

You'll be working with nba, a data set containing the names and ages of National Basketball Association (NBA) players from 2013, along with some statistics.

-   Write a linear search algorithm to find "Kobe Bryant" in the nba data set.
    -   The first column (index 0) contains each player's name.
    -   Once the algorithm finds "Kobe Bryant", store his position (from the second column) in the variable kobe\_position.

Let's first write it in pandas

```python
import pandas as pd
import numpy as np

path = "./data/nba_2013.csv"

nba_2013 = pd.read_csv(path)

kobe_position = nba_2013["pos"][nba_2013["player"] == "Kobe Bryant"]

kobe_position
```

{{% panel theme="success" header="Results" %}}
68    SG

Name: pos, dtype: object
{{% /panel %}}


With more vanilla Python

```python
# When the algorithm finds Kobe in the data set, store his position in Kobe_position
kobe_position = ""

# Find Kobe in the data set
kobe_position = ""
for row in nba:
    if row[0] == "Kobe Bryant":
        kobe_position = row[1]
```
