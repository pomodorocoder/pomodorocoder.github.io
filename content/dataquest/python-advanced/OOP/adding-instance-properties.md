+++
title = "Adding Instance Properties"
lastmod = 2017-11-14T10:18:50-05:00
categories = ["dataquest"]
weight = 4003
draft = false
+++

Now that we have a Team class with a team name, we can also store a team roster within each Team instance.

We'll represent a roster as a list of Player instances. We can write code inside the `__init__` method to run some initialization logic.

Modify the <span class="underline"><span class="underline">init</span></span> method of the Team class to loop through our data set and add a player to the roster every time the row's team name matches the instance's team\_name.

-   You can add an item to a list using .append(item).
-   Store the "San Antonio Spurs" team in spurs.

```python
class Player():
    # The special __init__ function runs whenever a class is instantiated
    # The init function can take arguments, but self is always the first one
    # Self is just a reference to the instance of the class
    # It is automatically passed in when you instantiate an instance of the class
    def __init__(self, data_row):
        self.player_name = data_row[0]
        self.position = data_row[1]
        self.age = int(data_row[2])
        self.team = data_row[3]

# Initialize a player using the first row of our data set
first_player = Player(players.iloc[0])

class Team():
    def __init__(self, team_name):
        self.team_name = team_name
        # Team roster initially empty
        self.roster = []
        # Find the players for the roster in the data set
        for row in players.iterrows():
            if team_name == row[-1][3]:
                self.roster.append(row[-1][0])

spurs = Team("Oklahoma City Thunder")
spurs.roster
```


{{% panel theme="success" header="Results" %}}
['Steven Adams', 'Nick Collison', 'Kevin Durant', 'Derek Fisher', 'Ryan Gomes', 'Serge Ibaka', 'Royal Ivey', 'Reggie Jackson', 'Perry Jones', 'Jeremy Lamb', 'Kendrick Perkins', 'Andre Roberson', 'Thabo Sefolosha', 'Mustafa Shakur', 'Hasheem Thabeet', 'Russell Westbrook', 'Reggie Williams']
{{% /panel %}}



