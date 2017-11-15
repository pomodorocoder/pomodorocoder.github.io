+++
title = "Convert String to Binary"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T14:44:02-05:00
categories = ["dataquest"]
weight = 4005
draft = false
+++

Computers store strings in binary, just like they do with integers. First, they split them into single characters, then convert those characters to integers. Finally, they convert those integers to binary and store them.

We'll look at simple characters first - the so called ASCII characters. These include all upper and lowercase English letters, digits, and several punctuation symbols.

-   We can use the `ord()` function to get the integer for an ASCII character.
-   Then, we use the `bin()` function to convert to binary.

```python
binary_w = bin(ord("w"))
binary_w
```


{{% panel theme="success" header="Results" %}}0b1110111{{% /panel %}}


```python
binary_bracket = bin(ord("}"))
binary_bracket
```

{{% panel theme="success" header="Results" %}}0b1111101{{% /panel %}}

