---
title: "Cases"
cascade:
  type: "docs"
---

This is a summary of all cases.  Note that a cases is a pair of a _pattern_ which describes how indidivual words are cased, and a _delimiter_ which describes how those words are joined.

Here is a summary of common cases used in programming languages, as described by their pattern and delimiter.

| pattern | underscore `_` | hyphen `-` | no delimiter |
| --- | --- | --- | --- |
| lower | [snake_case](snake) | [kebab-case](kebab) | [flatcase](flat) |
| upper | [CONSTANT_CASE](upper_snake) | [COBOL-CASE](cobol) | [UPPERFLATCASE](upper_flat) |
| capital | | [Train-Case](train) | [PascalCase](pascal) |
| camel | | | [camelCase](camel) |

## Other Cases

We can also consider space as a delimiter.  In the context of programming languages, spaces are almost universally used to distiguish tokens from one another, meaning you couldn't use a space as part of an identifier.

But outside the context, we might prepare an identifier to printing to an end user or logging to a file.  In the formatting sense, considering space as a delimiter is useful.  We can give these names as well.

| pattern | space |
| --- | --- |
| lower | [lower case](lower) |
| upper | [UPPER CASE](upper) |
| capital | [Title Case](title) |

We also can consider the sentence pattern.  With a space delimiter, this describes how arabic languages case sentences.

| pattern | space |
| --- | --- |
| sentence | Sentence case |

Sentence pattern used with other delimiters might also be seen used.  Many computer users might name files following a case that uses sentence pattern with underscores or hypthens as delimiters.  These cases do not have a common name.

## Non-Cases

If you ignore the formal definition of a case and consider only colloquial use of cases, we get a list of exotic cases that are used in non-programming contexts.

| name | example |
| --- | --- |
| alternating | aLtErNaTiNg CaSe |
| random | ranDom CAsE |
| toggle | tOGGLE cASE |
| surreal | s u r r e a l c a s e |

Furthermore, if we consider the idea of prefixes and suffixes, some programming languages that use symbols to prefix identifiers sometimes consider those identifiers to follow a different case.  For example, [Python PEP 0008](https://peps.python.org/pep-0008/#descriptive-naming-styles) defines a list of conventions, some of which we would define as cases, along with names for identifiers with underscore prefixes, such as `__double_leading_underscore` and `single_trailing_underscore_`.
