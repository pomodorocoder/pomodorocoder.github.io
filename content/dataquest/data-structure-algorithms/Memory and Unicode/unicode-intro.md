+++
title = "Unicode Intro"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:04:28-05:00
categories = ["dataquest"]
weight = 4006
draft = false
+++

What happened to all of the other characters and alphabets in the world. ASCII can't handle them, because it only supports 255 characters. The tech community realized it needed a new standard, and created Unicode.

Unicode assigns "code points" to characters. In Python, code points look like this: `"\u3232"`

We can use an encoding system to convert these code points to binary integers. The most common encoding system for Unicode is UTF-8. This encoding tells a computer which code points are associated with which integers.

UTF-8 can encode values that are longer that one byte, which enables it to store all Unicode characters. It encodes characters using a variable number of bytes, which means that it also supports regular ASCII characters (which are one byte each).

```python
binary_1019 = bin(ord('\u1019'))
binary_1019
```


{{% panel theme="success" header="Results" %}}0b10011111110110{{% /panel %}}
