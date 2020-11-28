+++
title = "String Case"
+++

Multiword identifiers require a case to distinguish meaning between words while still remaining a single token.  We define the variety of cases, when they are used, and set a standard naming convention.

A simple classification of possible cases is the casing of each word and the character used to join them.

| | underscore `_` | hyphen `-` | empty delimeter |
| --- | --- | --- | --- |
| lowercase | [snake_case](/case/snake) | kebab-case | flatcase |
| UPPERCASE | UPPER_SNAKE_CASE | COBOL-CASE | UPPERFLATCASE |
| Capitalized | Pascal_Snake_Case | Train-Case | PascalCase |

However, this fails to identify cases where an identifier contains words of multiple casings, like camelCase, which contains a lowercase and a capitalized word.  We describe two additional patterns: camel, where the first word is lowercase and the rest are capitalized, and sentence, where the first word is capitalized and the rest are lowercase.

| | underscore `_` | hyphen `-` | empty delimeter |
| --- | --- | --- | --- |
| camel Pattern | unnamed_Case | unnamed-Case | camelCase |
| Sentence pattern | Bjarne_case | Bjarne-bab-case | Unnamedcase |

See that these names are either unclassified or perhaps unheard of.  Further research is required to determine a practical name.  Please reach out if you have evidence of these cases being used in practice, and what it might be called.

One might consider other stylistic ways to print a string, although their use for an identifier is impractical or absurd.  This includes the space-delimited cases, some of which are not listed here.

| | |
| --- | --- |
| title | Title Case |
| alternating | aLtErNaTiNg CaSe |
| random | ranDom CAsE |
| toggle | tOGGLE cASE |
| surreal | s u r r e a l c a s e |

This website is a project to formally define these cases and set naming conventions while siting a history of their usage in computing.
