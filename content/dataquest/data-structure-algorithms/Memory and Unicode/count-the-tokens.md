+++
title = "Count the tokens"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T16:47:29-05:00
categories = ["dataquest"]
weight = 4017
draft = false
+++

Now that we've filtered the tokens, we can count how many times each one occurs. The Counter object from the collections library will help us with this.

Counter takes a list as input. It creates a dictionary where the keys are list items, and the values are the number of times those items appear in the list.

-   Count the items in filtered\_tokens and assign the result to filtered\_token\_counts
-   Get the three most common items in filtered\_token\_counts, and assign the result to common\_tokens.

```python
from collections import Counter
filtered_token_counts = Counter(filtered_tokens)
common_tokens = filtered_token_counts.most_common(3)
common_tokens
```

| Top Tokens    | Counts |
|---------------|--------|
| interrogation |    391 |
| information   |    375 |
| REDACTED      |    375 |
