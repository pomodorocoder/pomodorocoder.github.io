+++
title = "Intro"
date = 2017-11-10T00:00:00-05:00
lastmod = 2017-11-10T17:18:24-05:00
categories = ["dataquest"]
weight = 4001
draft = false
+++

In this mission, we'll learn how computers store values in memory.
We will look at the CIA memos data.
Here's a preview of the data

```python
year,statement,,,
1997,"The FBI information included that al-Mairi's brother ""traveled to Afghanistan in 1997-1998 to train in Bin - Ladencamps.""",,,
1997,"The FBI information included that al-Mairi's brother ""traveled to Afghanistan in 1997-1998 to train in Bin - Ladencamps.""",,,
```

The file consists of one long string. To use it effectively, we'd need to parse it and convert it into rows and columns. Here's a brief overview of how a computer stores the data:

-   Computers store files on hard drives
-   A hard drive allows us to save data, turn the computer off, and then access the data again later
-   The tech community commonly refers to hard drives as magnetic storage, because they store data on magnetic strips
-   Magnetic strips can only contain a series of two values - up and down. Our entire CSV file saves to a hard drive the same way. We can't directly write strings such as the letter a to a hard disk; we need to convert them to a series of magnetic ups and downs first.
-   We can do this with an encoding system called binary. With binary, the only valid numbers are 0 and 1. This constraint makes it easy to store binary values on a hard disk.
