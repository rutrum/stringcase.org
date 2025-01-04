---
title: "Cases"
cascade:
  type: "docs"
---

A string case is the pair of a _pattern_ which describes how individual words are cased and of a _delimiter_, a string that joines words together.

Below is a summary of common cases used in programming languages, as described by their pattern and delimiter.

| pattern | underscore `_` | hyphen `-` | no delimiter |
| --- | --- | --- | --- |
| lower | [snake_case](snake) | [kebab-case](kebab) | [flatcase](flat) |
| upper | [CONSTANT_CASE](upper_snake) | [COBOL-CASE](cobol) | [UPPERFLATCASE](upper_flat) |
| capital | | [Train-Case](train) | [PascalCase](pascal) |
| camel | | | [camelCase](camel) |

## Other Cases

We can also consider space as a delimiter.  In the context of programming languages, spaces are almost universally used to distiguish tokens from one another, meaning you couldn't use a space as part of an identifier.

We might still prepare an identifier for printing to an end user or logging to a file.  In the formatting sense, considering space as a delimiter is useful.  We can give these names as well.

| pattern | space |
| --- | --- |
| lower | [lower case](lower) |
| upper | [UPPER CASE](upper) |
| capital | [Title Case](title) |

We also can consider the sentence pattern.  With a space delimiter, this describes how many languages case sentences by capitalizing the first word.

| pattern | space |
| --- | --- |
| sentence | Sentence case |

Sentence pattern used with other delimiters might also be seen used.  Many computer users might name files following a case that uses sentence pattern with underscores or hypthens as delimiters.  These cases do not have a common name, as far as the author is aware.

## Non-Cases

Some "cases" are either not practical for programming or break the formal definition of a case.  These transformations still depend on the word-by-word or letter-by-letter transformations of case.  They are niche.

| name | example |
| --- | --- |
| alternating | aLtErNaTiNg CaSe |
| random | ranDom CAsE |
| toggle | tOGGLE cASE |
| surreal | s u r r e a l c a s e |

Furthermore, if we consider the idea of prefixes and suffixes, some programming languages that use symbols to prefix identifiers sometimes consider those identifiers to follow a different case.  For example, [Python PEP 0008](https://peps.python.org/pep-0008/#descriptive-naming-styles) defines a list of conventions, some of which we would define as cases, along with names for identifiers with underscore prefixes, such as `__double_leading_underscore` and `single_trailing_underscore_`.
