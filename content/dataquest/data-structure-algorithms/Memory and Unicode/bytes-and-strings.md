+++
title = "Bytes and Strings"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:31:35-05:00
categories = ["dataquest"]
weight = 4012
draft = false
+++

There's no encoding system associated with the bytes data type. That means if we have an object with that data type, Python won't know how to display the (encoded) code points in it. For this reason, we can't mix bytes objects and strings together.

```python
hulk_bytes = "Bruce Banner␦".encode("utf-8")

# We can't mix strings and bytes
# For instance, if we try to replace the Unicode ␦ character as a string, it won't work, because that value has been encoded to bytes
try:
    hulk_bytes.replace("Banner", "")
except Exception:
    print("TypeError with replacement")

# We can create objects of the bytes data type by putting a b in front of the quotation marks in a string
hulk_bytes = b"Bruce Banner"
# Now, instead of mixing strings and bytes, we can use the replace method with bytes objects instead
hulk_bytes.replace(b"Banner", b"")

thor_bytes = b"Thor"
thor_bytes
```

{{% panel theme="success" header="Results" %}}Thor{{% /panel %}}


Once we have a bytes object, we can decode it into a string using an encoding system. We use the .decode() method to do this.

```python
# Make a bytes object with aquaman's secret identity
aquaman_bytes = b"Who knows?"

# Now, we can use the decode method, along with the encoding system (UTF-8) to turn it into a string
aquaman = aquaman_bytes.decode("utf-8")

# We can print the value and type to verify that it's a string
print(aquaman)
print(type(aquaman))

morgan_freeman_bytes = b"Morgan Freeman"

morgan_freeman = morgan_freeman_bytes.decode("utf-8")

morgan_freeman
```


{{% panel theme="success" header="Results" %}}
Who knows?

class 'str'

Morgan Freeman
{{% /panel %}}

