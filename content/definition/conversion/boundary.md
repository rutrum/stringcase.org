+++
title = "Boundary"
weight = 12
+++

We say a _boundary_ is some condition that splits an identifier into a list of words.

Some boundaries _consume_ some string that is no longer present in the output strings, while others maintain the characters after splitting.

A boundary is a regex expression, then a start and end index for how to split the string.

Three parts to a boundary:
* the condition: a function that takes a slice of the identifier and returns true if the boundary condition is met
* the index of the end of one word `a`
* the index of the start of the next word `b`

Suppose an identifier I is sliced from index j onwards, so `S = I[j:]`.  Then if `S` meets the condition we return two words `S[:j+a]` and `S[j+b:]`.

Example, suppose we want to split `varName` into `var` and `name`.  We pass each slice `varName`, `arName`, `rName`, etc. into the boundary condition.  Then the boundary checks for some i if S[i] is lower and S[i+1] is upper.  If it is, then we split using indexes, where the first character match is 0.  We would then say we end the first string at 1 and start the next string at 1.  Together, the boundary is this function, plus two bounds.

For `var-name`, we just check if S[i] is hyphen.  If it is, then we end the first string at 0 (excluding the hyphen) and start the next string at 1, after the hyphen. We might say that the boundary is `(lambda s: s[0] == "-", 0, 1)`.
