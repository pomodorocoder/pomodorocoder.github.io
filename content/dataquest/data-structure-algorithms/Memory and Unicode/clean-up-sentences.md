+++
title = "Clean up Sentences"
date = 2017-11-13T00:00:00-05:00
lastmod = 2017-11-13T16:29:08-05:00
categories = ["dataquest"]
weight = 4015
draft = false
+++

Now that we've formatted our data nicely, we need to process the strings to count term occurences.

First, though, we need to clean them up by removing extraneous symbols. We only really care about letters, digits, and spaces.

Luckily, we can check the integer code of each character using ord() to see if it's a character we want to keep.

```python
# The integer codes for all the characters we want to keep
good_characters = [48, 49, 50, 51, 52, 53, 54, 55, 56, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 32]

sentences_cia = df.copy()

sentence_15 = sentences_cia["statement"][14]

# Iterate over the characters in the sentence, and only take those whose integer representations are in good_characters
# This will construct a list of single characters
cleaned_sentence_15_list = [s for s in sentence_15 if ord(s) in good_characters]

# Join the list together, separated by "" (no space), which creates a string again
cleaned_sentence_15 = "".join(cleaned_sentence_15_list)

# Define the clean function
def clear_str(my_str):
    temp_str = [s for s in my_str if ord(s) in good_characters]
    return "".join(temp_str)

sentences_cia["cleaned_statement"] = sentences_cia["statement"].apply(clear_str)
sentences_cia.head()
```
| year | statement                                         | cleaned\_statement                                |
|------|---------------------------------------------------|-------------------------------------------------- |
| 1997 | The FBI information included that al-Mairi's b... | The FBI information included that alMairis bro... |
| 1997 | The FBI information included that al-Mairi's b... | The FBI information included that alMairis bro... |
| 1997 | For example, on October 12, 2004, another CIA ... | For example on October 12 2004 another CIA det... |
| 1997 | On October 16, 2001, an email from a CTC offic... | On October 16 2001 an email from a CTC officer... |
| 1997 | For example, on October 12, 2004, another CIA ... | For example on October 12 2004 another CIA det... |

Now we need to combine the sentences and convert them to tokens.

The eventual goal is to count up how many times each term occurs.

```python
combined_statements = " ".join(sentences_cia["cleaned_statement"])
statement_tokens = combined_statements.split(" ")
statement_tokens[:10]
```

|     |     |             |          |      |          |         |          |    |             |
|-----|-----|-------------|----------|------|----------|---------|----------|----|-------------|
| The | FBI | information | included | that | alMairis | brother | traveled | to | Afghanistan |
