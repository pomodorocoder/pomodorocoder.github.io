+++
title = "The Basics of Binary"
date = 2017-11-10T00:00:00-05:00
lastmod = 2017-11-10T17:18:30-05:00
categories = ["dataquest"]
weight = 4002
draft = false
+++

Computers can't store values like strings or integers directly. Instead, they store information in binary, where the only valid numbers are 0 and 1. This system makes storing data on devices like hard drives possible.

-   Base 10: we normally count in "base 10." We call this system base 10 because there are 10 possible digits - 0 through 9
-   Base 2: Binary is base two, because there are only two possible digits - 0 and 1

Let's explore how binary numbers work. Convert the binary number "100" to a base 10 integer, and assign the result to `base_10_100`

-   In python, we have to store binary numbers as strings.
-   If we try to enter it directly as b = 10, Python will assume it's a base 10 integer
-   we can convert b from a string to a binary number with the `int` function
    -   We need to set the optional second argument, base, to 2 (binary is base two)

```python
base_10_100 = int("100", 2)
base_10_100
```

{{% panel theme="success" header="Results" %}}4{{% /panel %}}
