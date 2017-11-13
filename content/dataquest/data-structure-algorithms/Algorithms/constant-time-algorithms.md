+++
title = "Constant Time Algorithms"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T18:42:45-05:00
categories = ["dataquest"]
weight = 4006
draft = false
+++

A constant algorithm takes the same amount of time to complete, regardless of the input size.

For example, let's consider an algorithm that returns the first element of a list:

```python
def first(ls):
    return ls[0]
```

Regardless of list size, the algorithm returns the first element in constant time. It only takes one operation to retrieve this element, no matter how large the list.

We tend to think of algorithms in terms of steps. We consider any basic operation like setting a variable or performing arithmetic a step. **Algorithms that take a constant number of steps are always constant time, even if that constant number is not 1.**

Most complicated algorithms are not constant time. However, many operations within larger algorithms are constant time. Since we don't particularly care about what the constant is, we don't need to tediously count steps, as long as we're certain we'll get a constant.

An example of an operation that's not constant time is a loop that touches every element in an input list. Since a larger input would necessitate more steps, we can't treat this operation as a constant. We'll look closely at cases like this soon.
