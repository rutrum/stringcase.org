+++
title = "Case Conversion"
math = true
weight = 15

[sidebar]
open = true
+++

_Case conversion_ is the process that maps a string with a known case _x_ into a string with another case _y_ such that the words present in the identifier are constant.  **Is this true? For flatcase?** 

Conversion happens in two steps:

1. _Segmentation_: an identifier is split into a list of words
2. _Generation_: a list of words is converted into an identifier as defined by a given case

Generation itself happens in two steps:

1. _Mutation_: each word is transformed based on the pattern of the case
2. _Joining_: each word is joined into a single identifier based on the delimiter of the case

Mathematically speaking, we say the following.

We say that $\mathcal W$ is the space of all lists of words and $\mathcal I$ is the space of all identifiers.  We say $c \in \mathcal C$ is some case.  Then $c = (p, d)$ for some pattern $p \in \mathcal P$ and delimiter $d \in \mathcal D$.  We say that $B$ is a set of conditions under which we split an identifier into words.

$$\text{mutate}: \mathcal W \rightarrow_p \mathcal W$$
$$\text{join}: \mathcal W \rightarrow_d \mathcal I$$
$$\text{segment}: \mathcal I \rightarrow_B \mathcal W$$

Then we can finally define a _converter_ as a function that performs case conversion.

$$\text{converter}: \mathcal I \rightarrow_c\mathcal I$$

**Question: what does it mean for an identifier to inherantly HAVE a case?**
