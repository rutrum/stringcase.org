+++
title = "Pattern"
weight = 3
type = "docs"
math = true
+++

A _pattern_ is a function that maps a list of words into another list of words, usually performing some mutation on letter on a word-by-word basis.

Patterns can most easily be described as a series of word cases to transfer the input into.  Below is a list of common patterns and how they could be defined from word cases.

| pattern name | series |  example |
| --- | --- | --- |
| lower | lower, lower, ... | my word list |
| upper | upper, upper, ... | MY WORD LIST |
| capitalized | capitalized, capitalized, ... | My Word List |
| sentence | capitalized, lower, lower, ... | My word list |
| camel | lower, capitalized, capitalized, ... | my Word List |

Broadly speaking, a _pattern_ is just a function, and doesn't need to follow word cases, and could be dependent on the number of words, for instance.  However, it is a requirement that the newly mapped space contain the same number of words.  

Let $W_n$ be the space of lists of words that are of length $n$.  Then a pattern can defined as

$$pattern: W_n \rightarrow W_n$$