+++
title = "Hexadecimal Conversions"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:21:05-05:00
categories = ["dataquest"]
weight = 4010
draft = false
+++

Some notes on hexadecimal notions:

-   The `\x` prefix means "the next two digits are in hexadecimal."
-   Two hexadecimal digits equal eight binary digits, because digits can have higher values in hexadecimal (base 16). For instance, "F" is 15 in hexadecimal, but 1111 is 15 in binary.
-   Because it's shorter to display, and four binary digits always equal one hexadecimal digit, programs often use hexadecimal to print out values. This is purely for convenience.

```python
# F is the highest single digit in hexadecimal (base 16)
# Its value is 15 in base 10
print(int("F", 16))

# A in base 16 has the value 10 in base 10
print(int("A", 16))

# Just like the earlier binary_add function, this adds two hexadecimal numbers
def hexadecimal_add(a, b):
    return hex(int(a, 16) + int(b, 16))[2:]

# When we add 1 to 9 in hexadecimal, it becomes "a"
value = "9"
value = hexadecimal_add(value, "1")
print(value)

hex_ea = hexadecimal_add("ea", "2")
print(hex_ea)

hex_ef = hexadecimal_add("f", "e")
print(hex_ef)
```


{{% panel theme="success" header="Results" %}}
15

10

a

ec

1d
{{% /panel %}}
