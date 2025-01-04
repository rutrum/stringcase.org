+++
title = "Case"
weight = 5
sidebar.open = true
math = true
+++

A _multi-word identifier_ is a string composed of one or more words.  Representing words as a single identifier involves joining words together, typically in a manner than makes the individual words distinguishable from one another.  But the identifier is only a string, and doesn't contain any metadata about the words used.  For this reason, we can call a multi-word identifier just a _string_.

When representing words as a single identifier, each word is formatted with a certain word case, then joined together with a delimiter.  This pattern along with the a delimeter is what we define as a _string case_, or simply, a _case_.

$$\text{case} \coloneqq (\text{pattern}, \text{delimiter})$$

This definition aligns with colloquial uses of variable cases in programming languages.  For example, _snake case_ is the lower pattern with underscore delimiter.  For a list of names given to particular pattern-delimiter pairs, see [cases](/cases).
