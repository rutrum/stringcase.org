+++
title = "Pattern"
weight = 3
type = "docs"
math = true
+++

A _pattern_ is a series of word cases.  It describes how each word in a multiword identifier is cased.

The following is a table of cases:

| pattern name | series |  example |
| --- | --- | --- |
| lower | lower, lower, ... | my word list |
| upper | upper, upper, ... | MY WORD LIST |
| capitalized | capitalized, capitalized, ... | My Word List |
| sentence | capitalized, lower, lower, ... | My word list |
| camel | lower, capitalized, capitalized, ... | my Word List |

A series isn't the most precise definition.  A series assumes we have a list of words of undefined length, or arbitrary length.  In practice, multiword identifiers have a known fixed length.  We could more generally define a pattern as a function takes a known length $n$ and produces a list of word cases with length $n$.

For example, we would define a pattern where the final word is uppercase, but all previous words are lowercase.

**todo: consider redefining pattern and wordcase to be functions of the length of the word list/word**
