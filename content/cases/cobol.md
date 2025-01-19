+++
title = "COBOL-CASE"
weight = 21
+++

_Cobol case_ is the upper pattern with hyphen `-` delimiter.

Cobol case is also known as _upper kebab case_.

**todo** not sure Cobol case is even a great name

## History

Named after it's frequent use in the Cobol programming language.  In modern programming languages this case is rarely used, usually since the minus sign is used for subtraction and can't be used in identifiers.

## Usage

In Cobol, hyphens are allowed in identifiers.  It is not required to use Cobol case for identifiers, but it is common.
```
01 CUSTOMER-NAME PIC A(6) VALUE 'string'.
01 MEAL-COST PIC S9(3)V9(2) VALUE 120.39.
```