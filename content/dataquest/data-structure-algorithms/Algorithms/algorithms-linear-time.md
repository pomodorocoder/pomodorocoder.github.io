+++
title = "Algorithms Linear Time"
date = 2017-11-14T00:00:00-05:00
lastmod = 2017-11-14T08:32:29-05:00
categories = ["dataquest"]
weight = 4007
draft = false
+++

Accounting for the worst case scenario will ensure that the algorithm we choose or build is more robust.

In the worst case scenario for a list of size n, the algorithm has to check n elements. We refer to this time complexity as linear time because the runtime grows at a constant rate with respect to the size of the input.

Algorithms that take constant multiples of n steps (where n is the input size) are still linear time. For instance, an algorithm that takes 5n steps, or even 0.5n steps, is linear time. If we have an algorithm that prints the first half of a list (and we know the length of the list ahead of time), the algorithm will take 0.5n time. Even though it takes less than n time, we still consider it linear.

It's also worth noting that we only care about performance at a large scale. At a small scale, most algorithms will run pretty quickly, and it's only when n becomes large that we worry about time complexity.

Consequently, we only consider the highest order of n for time complexity. That means that an algorithm that runs in 9n + 20 time is linear, because the constant component is negligible for large values of n.

-   Example of A Linear Algorithm: Find the length of a list

```python
def length(ls):
    count = 0
    for elem in ls:
        count = count + 1
length_time_complexity = "linear"
```

-   Another Example of A Linear Algorithm: Check whether a list is empty -- Implementation 1

```python
def is_empty_2(ls):
    for element in ls:
        return False
    return True
is_empty_2_complexity = "linear"
```

-   Example of a Constant Algorithm: Check whether a list is empty -- Implementation 2

```python
def is_empty_1(ls):
    if length(ls) == 0:
        return True
    else:
        return False
is_empty_1_complexity = "constant"
```

So, if an internal function costs n operations, we must be sure to factor that into our time complexity analysis.
