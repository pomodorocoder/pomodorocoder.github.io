+++
title = "HexaDecimal Intro"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:16:20-05:00
categories = ["dataquest"]
weight = 4009
draft = false
+++

`batman_bytes` from the last screen prints out as `Bruce Wayne\xe2\x90\xa6`. Similar to the `\u` prefix for a Unicode code point, `\x` is the prefix for a hexadecimal character.

Just like binary is base 2 and our normal counting system is base 10, hexadecimal is base 16. The valid digits in hexadecimal are 0-9 and A-F. Here are the values corresponding to each character:

-   A - 10
-   B - 11
-   C - 12
-   D - 13
-   E - 14
-   F - 15

In hexadecimal, 9 + 1 equals A. We use hexadecimal because it represents a byte efficiently. You may recall that a byte is eight bits, or eight binary digits. The highest value we can express in a byte is 11111111, or 255 in base 10. We can express the same value in two hexadecimal digits, FF.

Programmers often use hexadecimal to display bytes instead of binary because it's more compact and easier to write out.
