+++
title = "Notation for Time Complexity"
date = 2017-11-14T00:00:00-05:00
lastmod = 2017-11-14T08:37:05-05:00
categories = ["dataquest"]
weight = 4008
draft = false
+++

When discussing time complexity, we should use the proper notation. Most commonly, we use **Big-O Notation**.

-   To denote constant time, we would write `O(1)`, because 1 is a constant (and a simple constant).
-   To denote linear time, we would write `O(n)`, because n is the simplest example of linearity.

Big-O Notation follows a similar pattern for other time complexities. For example, `O(n^2)`, `O(2^n)`, and `O(log(n))` are all valid notation. The algorithms with these complexities are probably rather complicated. For now, it's enough to be able to recognize Big-O Notation so we can use it to describe time complexities in future missions.

Time complexity is an important consideration when we're analyzing real-world data. An inefficient algorithm will perform very slowly on a large data set.

Algorithms with lower-order time complexities are more efficient. Constant time algorithms, which we denote with `O(1)`, are more efficient than linear time algorithms, which we denote with `O(n)`. Similarly, an algorithm with complexity `O(n^2)` is more efficient than one with complexity `O(n^3)`.

When considering algorithms, we always want to choose the one with the lowest time complexity. It may not always be the easiest one to implement, but the extra effort is usually worth the resulting efficiency.
