+++
title = "Delimiter"
weight = 4
+++

A _delimiter_ is an optional string of characters that join words together.  Common choices are strings of length one, such as period `.`, hyphen `-`, underscore `_`, or space.  It is also common to use an empty string.

The delimiter is used to distinguish words within an identifier.  When a delimiter is not used, the expectation is that the letter casing between adjacent characters of different words would be different, serving the same purpose.

When a empty string is used as a delimiter and the pattern doesn't distinguish the words from adjacent words, then information is lost about which words were used to build the identifier.  Similarly, a choice of delimiter that is not a symbol or whitespace, can also be ambiguous depending on what characters are used within a word.
