+++
title = "Case Conversion"
math = true
weight = 15

[sidebar]
open = true
+++

_Case conversion_ is the process that maps a string with a known case _x_ into a string with a _target case_ _y_ such that the words present in the identifier are constant.  **Is this true? For flatcase?** 

Conversion happens in three steps:

1. _Segmentation_: an identifier is split into a list of words
2. _Mutation_: each word is transformed based on a pattern
3. _Joining_: each word is joined into a single identifier using a delimiter

Mathematically speaking, we say the following.

We say that $\mathcal W$ is the space of all lists of words and $\mathcal I$ is the space of all identifiers.  We say $c \in \mathcal C$ is some target case.  Then $c = (p, d)$ for some pattern $p \in \mathcal P$ and delimiter $d \in \mathcal D$.  We say that $B$ is a set of conditions under which we split an identifier into words.

Then we say that conversion is composed of the following functions.

$$\text{segment}: \mathcal I \underset B\longrightarrow \mathcal W$$
$$\text{mutate}: \mathcal W \underset p\longrightarrow \mathcal W$$
$$\text{join}: \mathcal W \underset d\longrightarrow \mathcal I$$

And we define a conversion function _convert_, which maps one identifier to another based on boundaries conditions, a pattern, and a delimeter, as the following.

$$\text{convert} = \text{join}\circ\text{mutate}\circ\text{segment}: \mathcal I \underset {c, B}\longrightarrow \mathcal I $$
