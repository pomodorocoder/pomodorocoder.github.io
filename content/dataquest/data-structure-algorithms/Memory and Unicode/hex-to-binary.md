+++
title = "Hex to Binary"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:24:31-05:00
categories = ["dataquest"]
weight = 4011
draft = false
+++

We can convert hexadecimal to binary fairly easily. We can even use the `ord()` and `bin()` functions that helped us convert code points to binary.

```python
# One byte (eight bits) in hexadecimal (the value of the byte below is \xe2)
hex_byte = "â"

# Print the base 10 integer value for the hexadecimal byte
print(ord(hex_byte))

# This gives the exact same value. Remember that \x is just a prefix, and doesn't affect the value.
print(int("e2", 16))

# Convert the base 10 integer to binary
print(bin(ord("â")))

binary_aa = bin(ord("\xaa"))
print(binary_aa)

binary_ab = bin(ord("\xab"))
print(binary_ab)
```


{{% panel theme="success" header="Results" %}}
226

226

0b11100010

0b10101010

0b10101011
{{% /panel %}}
