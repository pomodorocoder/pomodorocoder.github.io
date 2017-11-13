+++
title = "Defining a Class"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T14:04:24-05:00
weight = 4002
draft = false
+++

-   What is a class in JS? A constructor
-   What does a class have
    -   properties
    -   methods
-   What does it do


### An Example {#an-example}

-   Define a house class (constructore)

```js
function Building(floors){      // Constructor
    this.what = "building";     // Properties (per instance)
    this.floors = floors;
}

// Make an instance
var myHouse = new Building(3)

console.log(myHouse.what)
console.log(myHouse.floors)

Building.prototype.countFloors = function(){ // Methods for all instances
    console.log("I have", this.floors, "floors")
};
console.log(myHouse.countFloors())
```
{{% panel theme="success" header="Results" %}}
building

3

I have 3 floors
{{% /panel %}}
