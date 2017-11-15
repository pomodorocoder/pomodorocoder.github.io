+++
title = "Instance Methods"
date = 2017-11-14T00:00:00-05:00
lastmod = 2017-11-14T10:53:30-05:00
categories = ["dataquest"]
weight = 4004
draft = false
+++

The Player and Team classes we've defined serve as blueprints that we can use to create instances of these classes. Classes and the instances of those classes, which are collectively known as objects, are fundamental to object-oriented programming.

We can define some of our own methods on a class. For example, if we want to compute the average age of the players on a team, we would write a method for the Team class that does this. However, because this number can be different for each team, we want to make sure the method acts individually on specific instances of the Team class. We call these methods instance methods.

For method declarations, the first argument to the method is always self, even though we don't explicitly pass in self when we call the method. self is a reference to the current object we're working with. It's useful when we want to access properties of that object within the method we're defining.

Write an `average_age()` method for the Team class that computes the average age of the Team instance.

-   We've provided a method, `num_players`, that returns the total number of players on a Team instance.
-   Store the result of calling `average_age()` on the "San Antonio Spurs" team in `spurs_avg_age`.

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

class Team_1():
    def __init__(self, team_name):
        self.team_name = team_name
        # Team roster initially empty
        self.roster = []
        # Find the players for the roster in the data set
        for row in players.iterrows():
            if self.team_name == row[-1][3]:
                self.roster.append(row[-1][0])

        # Find the number of players
    def num_players(self):
        count = 0
        for player in self.roster:
            count += 1
        return count

        # Find the average age
    def average_age(self):
        total_age = 0
        count = 0
        for row in players.iterrows():
            if self.team_name == row[-1][3]:
                total_age += int(row[-1][2])
                count += 1
        return (total_age / count)

spurs = Team_1("San Antonio Spurs")
spurs_num_players = spurs.num_players()
spurs_avg_age = spurs.average_age()
spurs_avg_age
```


{{% panel theme="success" header="Results" %}}
28
{{% /panel %}}
