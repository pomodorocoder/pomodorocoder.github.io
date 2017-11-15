+++
title = "Convert to a Pandas dataframe"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T16:01:57-05:00
categories = ["dataquest"]
weight = 4014
draft = false
+++

To make this easier for ourselves, let's convert our sentences to a pandas dataframe.

Having a dataframe will make processing and analysis much simpler because we can use the .apply() method.

```python
import pandas as pd
df = pd.read_csv(path+"sentences_cia.csv")
df = df.iloc[:,:2]
df.head()
```


|year|                                          statement|
|----|---------------------------------------------------|
|1997|  The FBI information included that al-Mairi's b...|
|1997|  The FBI information included that al-Mairi's b...|
|1997|  For example, on October 12, 2004, another CIA ...|
|1997|  On October 16, 2001, an email from a CTC offic...|
|1997|  For example, on October 12, 2004, another CIA ...|
