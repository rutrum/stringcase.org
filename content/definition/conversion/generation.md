+++
title = "Mutation and Joining"
weight = 1
math = true
+++

Given a set of words, to convert to an identifier of a target case we use _mutation_ as defined by the case pattern and _join_ based on the case delimiter.

## Mutation

The pattern of the case defines how to mutate each word in the word list.  Applying this pattern $p$ across a list of words is called _mutation_.

$$\text{mutate}: \mathcal W \underset p\longrightarrow \mathcal W$$

## Joining

The delimeter then describes how the words should be concatenated.  To perform joining, all words are concatenated together with a delimiter $d$ between each word.  This can be called interspersing.

$$\text{join}: \mathcal W \underset d\longrightarrow \mathcal I$$
