+++
title = "Most Common Token by Year"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T17:17:01-05:00
categories = ["dataquest"]
weight = 4018
draft = false
+++

Now put everything together, let's write a function the count the most common tokens by a selected year

```python
# sentences_cia has been loaded in.
# It already has the cleaned_statement column.
def most_common_year(my_year):
    my_df = sentences_cia[sentences_cia["year"] == my_year]
    combined_statements = " ".join(my_df["cleaned_statement"])
    statement_tokens = combined_statements.split(" ")
    filtered_tokens = [s for s in statement_tokens if len(s) >= 5]
    filtered_token_counts = Counter(filtered_tokens)
    common_tokens = filtered_token_counts.most_common(2)
    return common_tokens

common_2000 = most_common_year(2000)
common_2002 = most_common_year(2002)
common_2013 = most_common_year(2013)

common_2000
```

| Top tokens | Counts |
|------------|--------|
| Ahmad      |      9 |
| terrorist  |      9 |
