+++
title = "Word"
weight = 2
+++

Words are strings of characters that contain no whitespace.  In the context of a variable name, these are the words you use to describe it's function.  You would later combine these words into a single idenfier to use as a variable, function, file, etc.  The words themselves have colloquial meaning, but aren't used independently of the identifier they make up in compilation and file parsing.

## Word Case

A word is a series of characters.  A _word case_ is a series of character cases that describe how the word should be formatted.  Below are some names to specific word casings, but is not exhaustive.

| name | series | example |
| --- | --- | --- |
| lower | lower, lower, ... | `pig`, `ostrich`, `goat` |
| upper | upper, upper, ... | `CHICKEN`, `CRAB`, `BIRD` |
| capital | upper, lower, lower, ... | `Dog`, `Monkey`, `Ocelot` |

Colloquially, we would say a word `pig` follows lower case, or that `Monkey` is capital case.  For capital word case in particular, we say the word is capitalized.

This definition could be extended to include a word case that specifies _end_ behavior, like that the last character should be upper case, for instance.  Maybe, more generally, a word case a function that applies a letter case to each character.
