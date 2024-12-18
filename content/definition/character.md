+++
title = "Character"
weight = 1
+++

Characters can be classified in a variety of ways.  One could partition the ascii characters into digits, symbols, upper case letters, lower case letters, and non-printing characters.  Unicode is an incredibly robust standard that classifies all characters as well.  We'll simplify our analysis for the purpose of identifiers in programming languages, which are a bit more limited than the extent of all of unicode.  Something to loop back to.

Moving forward, we will define a _character_ as one of the [printable ascii characters](https://en.wikipedia.org/wiki/ASCII#Printable_characters).  We can partition these characters in the following classes:

* The space character (0x20)
* Digits 0-9 (0x30-0x39)
* Upper case letters (0x41-0x5A)
* Lower case letters (0x61-0x7A)
* Symbols, everything else

## Letter(?) Case

Should this be letter case or character case?  A "character" is important in terms of programming, but a "letter" is important in terms of linguistic usage.  What's more important?  Letter sounds great until I need to start defining edge cases for other no-case characters... Character may not even be accurate either, since in unicode we would call it a codepoint.

The upper and lower case letters both represent the same arabic letter.  We say these characters have a _letter case_ of either upper or lower.  The remaining characters of space, symbols, and digits do not have a letter case.

| name | examples |
| --- | --- |
| lower | `r`, `j`, `d` |
| upper | `R`, `J`, `D` |
| no case | `-`, `8`, `~`, space |
