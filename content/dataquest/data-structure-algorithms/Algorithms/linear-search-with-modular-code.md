+++
title = "Linear Search with Modular Code"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T18:36:51-05:00
categories = ["dataquest"]
weight = 4004
draft = false
+++

Now let's try writing a modular search function that can find the age of any player in our data set without having to repeat code.

-   Write a function called player\_age that takes in a name parameter.
    -   The function should return the player's age from the nba data set, which we've loaded in for you.
    -   If the function doesn't find the player, it should return -1.
    -   The third column of nba (index 2) contains the players' ages.
-   Store the age of "Ray Allen" in the variable allen\_age.
-   Store the age of "Kevin Durant" in the variable durant\_age.
-   Store the age of "Shaquille O'Neal" in the variable shaq\_age.

Again let's start with pandas

```python
def player_name_pd(name):
        return nba_2013["age"][nba_2013["player"] == name]

player_name_pd("Kobe Bryant")
```


{{% panel theme="success" header="Results" %}}
68    35

Name: age, dtype: int64
{{% /panel %}}

Again in Vanilla Python:

```python
# player_age returns the age of a player in our NBA data set
def player_age(name):
    for row in nba:
        if row[0] == name:
            return row[2]
    return -1

allen_age = player_age("Ray Allen")
durant_age = player_age("Kevin Durant")
shaq_age = player_age("Shaquille O'Neal")
```
