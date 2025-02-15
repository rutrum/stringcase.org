+++
title = "Case by Language Construct"
+++

Keep these headers alphabetized.  Maybe each section could become its own page.

## Pascal

From the GNU Pascal Coding Standards: https://www.gnu-pascal.de/h-gpcs-en.html

Flat here often implies that the identifier is only composed of a single word.  **Maybe "flat" should be distinguished here and instead cite that it should be a single word?** But maybe not.  Reserved words are already a fixed list that doesn't change.

feature | case
--- | ---
reserved words | flat
identifiers | Pascal
local variables | Pascal or flat
compiler directives | kebab

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