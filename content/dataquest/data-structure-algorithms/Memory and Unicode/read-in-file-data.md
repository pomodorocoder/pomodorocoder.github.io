+++
title = "Read in File Data"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T15:46:05-05:00
categories = ["dataquest"]
weight = 4013
draft = false
+++

Now that we understand Unicode, we can go ahead and read our data in.

```python
# We can read our data in using csvreader
import csv
path = "./data/"

# When we open a file, we can specify the system used to encode it (in this case, UTF-8).
f = open(path+"sentences_cia.csv", 'r', encoding="utf-8")
csvreader = csv.reader(f)
sentences_cia = list(csvreader)

# The data consists of two columns
# The first column contains the year, and the second contains a sentence from a CIA report written in that year
# Print the first column of the second row
print(sentences_cia[1][0])

# Print the second column of the second row
print(sentences_cia[1][1])
```


{{% panel theme="success" header="Results" %}}
1997

The FBI information included that al-Mairi's brother "traveled to Afghanistan in 1997-1998 to train in Bin - Ladencamps."
{{% /panel %}}
