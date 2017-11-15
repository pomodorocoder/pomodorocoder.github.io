+++
title = "Defining Custom Classes"
date = 2017-11-14T00:00:00-05:00
lastmod = 2017-11-14T09:11:47-05:00
categories = ["dataquest"]
weight = 4002
draft = false
+++

Let's take a look at how to use custom classes. We'll use them to explore data on NBA players from the 2013-2014 season. The statistics are in a CSV file with a header and some rows of data.

We need an easy way to represent both the players and the teams. Let's focus on how we can use custom classes to compare the average ages of the players on each team.

You can see in the starter code that we've defined a Player class and set up the default `__init__` method to accept a data row as an argument. We made a deliberate choice to split up the logic of players and teams so our code is easy to read and maintain. We also made the convenient choice to initialize our Player instances using a data row. That's because all of the information is present in a row, and it will make it easier to create Player objects from the data set later on.

First, let's load data

```python
import pandas as pd
players = pd.read_csv(path)
```

Create a Player Class

```python
class Player():
    def __init__(self, data_row):
        self.player_name = data_row[0]
        self.position = data_row[1]
        self.age = data_row[2]
        self.team = data_row[3]

first_player = Player(players.iloc[0])
first_player.player_name
```

{{% panel theme="success" header="Results" %}}Quincy Acy{{% /panel %}}

Several takeaways here:

-   The special `__init__` function runs whenever a class is instantiated
-   The `init` function can take arguments, but self is always the first one
-   self is just a reference to the instance of the class
-   It is automatically passed in when you instantiate an instance of the class

Create a Team class

```python
class Team():
    def __init__(self, data):
        self.team_name = data

spurs = Team("San Antonio Spurs")
spurs.team_name
```


{{% panel theme="success" header="Results" %}}San Antonio Spurs{{% /panel %}}
