+++
title = "Case by Language Construct"
+++

General resources:
* Google style guides: https://google.github.io/styleguide/
* Naming conventions on Rosetta Code: https://rosettacode.org/wiki/Naming_conventions

Keep these headers alphabetized.

## Bash

Google shell style guide: https://google.github.io/styleguide/shellguide.html#naming-conventions

feature | case
--- | ---
functions | snake
variables | snake
constants | constant
environment variables | constant
readonly variables | constant
filenames | snake or flat

## C

GNU standards for C code: https://www.gnu.org/prep/standards/html_node/Names.html#Names

feature | case
--- | ---
macros | constant
enums variants | constant
varables | snake
functions | snake

Linux kernel: https://www.kernel.org/doc/html/v4.10/process/coding-style.html

feature | case
--- | ---
macro constants | constant
enum labels | constant
macros | constant or flat

## C#

Microsoft: https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names

feature | case
--- | ---
types | Pascal
namespaces | Pascal
public members | Pascal
classes | Pascal
interfaces | Pascal
structs | Pascal
delegate | Pascal
variables | camel
private members | camel

## CSS

feature | case
--- | ---
identifiers | kebab

## Go

Effective Go: https://go.dev/doc/effective_go

feature | case
--- | ---
packages | flat
public items | Pascal
private items | camel
files | snake

## HTML

feature | case
--- | ---
tags | flat
attributes | flat
data attribute | kebab

## Java

Google style guide: https://google.github.io/styleguide/javaguide.html#s5.2-specific-identifier-names

feature | case
--- | ---
classes | Pascal
methods | camel
constants | constant
non-constant fields | camel
parameters | camel
local variables | camel
types | Pascal

## JavaScript

Google style guide: https://google.github.io/styleguide/jsguide.html#naming-rules-by-identifier-type 

feature | case
--- | ---
files | kebab or snake
packages | camel
classes | Pascal
methods | camel
enums | Pascal
enum variants | constant
constants | constant
non-constant fields | camel
parameters | camel
local variables | camel
template paramaters | upper flat


## Lisp

Assuming, for now, there isn't much difference between dialects.

Common lisp style guide: https://lisp-lang.org/style-guide/#naming

feature | case
--- | ---
identifiers | kebab
files | kebab

## Nim

Nim standard library style guide: https://nim-lang.org/docs/nep1.html

feature | case
--- | ---
types | Pascal
non-pure enum values | camel
pure enum values | Pascal
other identifiers | camel

## Pascal

From the GNU Pascal Coding Standards: https://www.gnu-pascal.de/h-gpcs-en.html

Flat here often implies that the identifier is only composed of a single word.  **Maybe "flat" should be distinguished here and instead cite that it should be a single word?** But maybe not.  Reserved words are already a fixed list that doesn't change.

feature | case
--- | ---
reserved words | flat
identifiers | Pascal
local variables | Pascal or flat
compiler directives | kebab

## Perl

Official documentation: https://perldoc.perl.org/perlstyle

feature | case
--- | ---
constants | constant
globals | Ada
locals | snake
functions | snake
methods | snake
modules | Pascal(?)

## PHP

This doesn't look comprehensive: https://www.php.net/manual/en/userlandnaming.rules.php

There's this too: https://www.php-fig.org/psr/psr-1/ and https://infinum.com/handbook/wordpress/coding-standards/php-coding-standards/naming

feature | case
--- | ---
functions | snake
classes | camel or Pascal
constants | constant
methods | camel
files | kebab or Pascal

## Python

PEP8 of course: https://peps.python.org/pep-0008/#descriptive-naming-styles

feature | case
--- | ---
modules | snake
packages | flat or snake
classes | Pascal
types | Pascal
globals | snake
functions | snake
variables | snake
arguments | snake
methods | snake
constants | constant

## R

This looks the most official, given that google forked it: https://style.tidyverse.org/

features | case
--- | ---
files | snake or kebab
variables | snake

It should also be noted that some built-in R methods using lowercase pattern with period (dot) delimiter.

## Ruby

This looks official: https://rubystyle.guide/#naming-conventions

feature | case
--- | ---
symbols | snake
methods | snake
variables | snake
classes | Pascal
modules | Pascal
files | snake
directories | snake
constants | constant

## Rust

Pretty clear: https://rust-lang.github.io/api-guidelines/naming.html

The style guide has more details about how each feature should be formatted or used, but I've simplified it here to just align with the most appropriate case.

feature | case
--- | --- 
crates | kebab or snake
modules | snake
types | Pascal
traits | Pascal
enum variants | Pascal
functions | snake
methods | snake
macros | snake
local variables | snake
constants | constant
statics | constant
type parameters | Pascal
lifetimes | flat

## Scala

Official scala style guide: https://docs.scala-lang.org/style/naming-conventions.html

feature | case
--- | ---
classes | Pascal
objects | Pascal
packages | flat
methods | camel
constants | camel
type parameters | Pascal
annotations | camel

## Standard ML

This person already wrote an excellent article doing this exact thing, by looking at 8 sources of style guides: https://thebreakfastpost.com/2016/06/11/naming-conventions-in-standard-ml/

His final recommendation is as follows:

feature | case
--- | ---
variables | camel
types | snake
datatype constructors | constant
exceptions | Pascal
structure | Pascal
signature | constant
functor | Pascal
files | kebab

## TypeScript

Google typescript style guide: https://google.github.io/styleguide/tsguide.html#naming-rules-by-identifier-type

feature | case
--- | ---
classes | Pascal
interfaces | Pascal
types | Pascal
enums | Pascal
decorators | Pascal
type parameters | Pascal
variables | camel
parameters | camel
functions | camel
methods | camel
properties | camel
module aliases | camel
constants | constant

## Vimscript

Google vimscript style guide: https://google.github.io/styleguide/vimscriptguide.xml?showone=Naming#Naming

feature | case
--- | ---
plugins | kebab
functions | Pascal
commands | Pascal
variables | snake