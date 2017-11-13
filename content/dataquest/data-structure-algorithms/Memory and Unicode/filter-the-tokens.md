+++
title = "Filter the Tokens"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T16:47:21-05:00
categories = ["dataquest"]
weight = 4016
draft = false
+++

The problem is that the most common words in the English language are ones that are relatively uninteresting to us right now -- words like "the", "a", and so on. These words are called stopwords - words that don't add much information to our analysis.

It's common to filter out any words on a list of known stopwords. What we'll do here for the sake of simplicity is filter out any words less than five characters long. This should remove most stopwords.

-   Filter the statement\_tokens list so that it only contains tokens that are at least five characters long.
-   Assign the result to filtered\_tokens.

```python
filtered_tokens = [s for s in statement_tokens if len(s) >= 5]
filtered_tokens[:10]
```
|             |          |          |         |          |             |       |            |             |          |
|-------------|----------|----------|---------|----------|-------------|-------|------------|-------------|----------|
| information | included | alMairis | brother | traveled | Afghanistan | train | Ladencamps | information | included |
