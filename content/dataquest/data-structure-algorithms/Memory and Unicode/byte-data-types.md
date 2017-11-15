+++
title = "The Byte Data Types"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:11:18-05:00
categories = ["dataquest"]
weight = 4008
draft = false
+++

Python includes a data type called "bytes." It's similar to a string, except that it contains encoded bytes values.

When we create an object with a bytes type from a string, we specify an encoding system (usually UTF-8).

Then, we can use the `.encode()` method to encode the string into bytes.

```python
# We can make a string with some Unicode values
superman = "Clark Kent␦"
print(superman)

# This tells Python to encode the string superman as Unicode using the UTF-8 encoding system
# We end up with a sequence of bytes instead of a string
superman_bytes = "Clark Kent␦".encode("utf-8")
print(superman_bytes)

batman = "Bruce Wayne␦"
batman_bytes = batman.encode("utf-8")
print(batman_bytes)
```


{{% panel theme="success" header="Results" %}}
Clark Kent␦

b'Clark Kent\xe2\x90\xa6'

b'Bruce Wayne\xe2\x90\xa6'
{{% /panel %}}
