+++
title = "Conversion"
weight = 11
math = true
draft = true
+++

When building a multiword identifier, we start with a series of words.  Then, we select a case under which to transform the series of words into a single identifier.  We call this _generation_.

We can also perform the inverse, which takes an identifier, and given a case can produce a series of words.  This is called _splitting_ (still working on this name.)

Well, when we consider generation, it's in two phases: mutation and joining.

Then, the inverse (not really) is just splitting, since we don't need to mutate the case, since that information is not important.  These functions are not necessarily inverses, since we can lose information.

Maybe use "segmentation".

If they are inverses, we might say that the generation was _invertible_.

I don't think I like the word "generation".

We say that a splitting followed by generation is called _case conversion_.

Let's use math here.

We say that $\mathcal W$ is the space of all lists of words and $\mathcal I$ is the space of all identifiers.  We say $c \in \mathcal C$ is some case.  Then $c = (p, d)$ for some pattern $p \in \mathcal P$ and delimiter $d \in \mathcal D$.  We say that $B$ is a set of conditions under which we split an identifier into words.

$$\text{mutate}: \mathcal W \rightarrow_c \mathcal W$$
$$\text{join}: \mathcal W \rightarrow_d \mathcal I$$
$$\text{split}: \mathcal I \rightarrow_B \mathcal W$$
