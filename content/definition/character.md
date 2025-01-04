+++
title = "Character"
weight = 1
+++

Characters can be classified in a variety of ways.  One could partition the ascii characters into digits, symbols, upper case letters, lower case letters, and non-printing characters.  Unicode is an incredibly robust standard that classifies all characters as well.  We'll simplify our analysis for the purpose of identifiers in programming languages, which are a bit more limited than the extent of all of unicode.  Something to loop back to.

Moving forward, we will define a _character_ as one of the [printable ascii characters](https://en.wikipedia.org/wiki/ASCII#Printable_characters).  We can partition these characters in the following classes:

* The space character (0x20)
* ASCII digits 0-9 (0x30-0x39)
* Uppercase Latin alphabet (0x41-0x5A)
* Lowercase Latin alphabet (0x61-0x7A)
* Symbols, everything else

In unicode terminology, we are going to consider only characters from the Basic Latin block. [^1]

## Letter Case

The unicode standard 16.0.0 describes a case as follows. [^2]

> Case is a normative property of characters in certain alphabets whereby characters
> are considered to be variants of a single letter.

In the context of the basic latin block, we only need to consider two variants of this case property.

> These variants, which may differ
> markedly in shape and size, are called the uppercase letter (also known as capital or
> majuscule) and the lowercase letter (also known as small or minuscule).

In the context of what we will define later as a string case, we call this property _letter case_.  All characters are one of _uppercase_, _lowercase_, or neither.  Characters that are neither uppercase or lowercase we say are _caseless_.

| letter case | examples |
| --- | --- |
| lowercase | `a`, `b`, `c`, ..., `z` |
| uppercase | `A`, `B`, `C`, ..., `Z` |
| caseless | `0`,...,`9`, `_`, `-`, space, etc. |

**todo: should letter case be two words?**
[^1]: [Unicode C0 Controls and Basic Latin](https://www.unicode.org/charts/PDF/U0000.pdf)
[^2]: [Unicode Standard 16.0.0: 4.2 Case](https://www.unicode.org/versions/Unicode16.0.0/UnicodeStandard-16.0.pdf#%5B%7B%22num%22%3A3932%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C36%2C594%2C0%5D)
