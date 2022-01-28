+++
title = "Some Definitions"
+++

# Characters

Characters can be classified in a variety of ways.  One could partition the ascii characters into digits, symbols, upper case letters, lower case letters, and non-printing characters.  Unicode is an incredibly robust standard that classifies all characters as well.  We'll simplify our analysis for the purpose of "multiword identifiers" in programming languages, which are a bit more limited than the extent of all of unicode.  Something to loop back to.

Three classes of characters:

* Lower case letters
* Upper case letters
* Everything else

That is, you can either be upper case, lower case, or neither.  Symbols, digits, and a variety of characters in non-romantic languages (like Chinese for example) have no sense of "letter case".  We will say each of the classes has the letter case of the following.

| | |
| --- | --- |
| Lowercase | `r`, `j`, `d` |
| Uppercase | `R`, `J`, `D` |
| No letter case | `-`, `8`, `~`, whitespace |

# Words

Words are strings of characters that contain no whitespace.  We can classify a variety of _word casings_ where the character follow some pattern of letter casing.

| | |
| --- | --- |
| Lowercase | `pig`, `ostrich`, `goat` |
| Uppercase | `CHICKEN`, `CRAB`, `BIRD` |
| Capital | `Dog`, `Monkey`, `Ocelot` |

# Multiword Identifiers

Multiword identifiers are strings that contain, in meaning, one or more words.  These have what we will simply call a _case_.  Given a list of words, we have two decisions about how to combine them into a single identifier.  Each word can have a unique word case and how the words are combined together via a delimeter.  It is these two characteristics that uniquely define a case.

We will call a _pattern_ a series of word casings.  We call a delimeter a string.  For example, if we have a pattern (Lowercase, Lowercase, ...) and a delimeter "_" (underscore) then we can use those to take a list of words ("my", "variable", "name") and construct a multiword identifier with a case defined by the pattern and delimeter: `my_variable_name`.  In this example, the pattern and delimeter pair we described is what is called "snake case".

There are a number of patterns of interest.  I will give them names here.

| | |
| --- | --- |
| lowercase pattern | Lowercase, Lowercase, ... |
| UPPERCASE PATTERN | Uppercase, Uppercase, ... |
| Capital Pattern | Capital, Capital, ... |
| camel Pattern | Lowercase, Capital, Capital, ... |
| Sentence pattern | Capital, Lowercase, Lowercase, ... |

If we match those with some popular delimeters, then we get a lot cases you might be familiar with.

| | "_" | "-" | "" |
| --- | --- | --- | --- |
| lowercase pattern | snake_case | kebab-case | flatcase |
| UPPERCASE PATTERN | SCREAMING_SNAKE_CASE | COBOL-CASE | UPPERFLATCASE |
| Capital Pattern | | Train-Case | PascalCase |
| camel Pattern | | | camelCase |
| Sentence pattern | | | |

The empty spots are things I've not come across to have names.  It would be nice to give these names based on their usage in programming languages.  For example, I've heard Train-Case also called HTTP-Header-Case.  Both are valid, although I think there should be an agreement, if possible, on a primary name.  I've also heard SCREAM_SNAKE_CASE called CONSTANT_CASE as well.

There are additional delimeters that can be examined, such as space.  These are less useful for applications in programming language syntax.

In addition, other patterns could be considered.  Similarly, different word casings could be used.  Some other possible word casings that come to mind are alternating letter casing and what would happen if you were using CAPS lock and didn't realize it.  Again, not as practical.

| | |
| --- | --- |
| Alternating | Lowercase, Uppercase, Lowercase, Uppercase, ... |
| Toggle | Lowercase, Uppercase, Uppercase, ... |

But the core of this discussion is that a _multiword identifier case_, or simply _case_ is the pair a of delimeter, a string, and a pattern, or series of word cases.
