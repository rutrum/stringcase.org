+++
title = "Case Boundaries"
weight = 20
math = true
+++

After converting words "Var" and "Name" into a kebab case identifier "var-name", we natural ask how we can return the identifier back into words, knowing that it is already kebab case?

There is a natural association between cases and boundaries that would split the identifier.  We will call these _case boundaries_ and can be considered an additional part of the case definition.

$$\text{case} \coloneqq (\text{pattern}, \text{delimiter}, \text{boundaries})$$

This additional information allows us not only to define **generation** in terms of a case, but also **segmentation**.  For instance, segmenting identifier `my-var_name` based on snake case would involve splitting upon and removing the underscore only, yielding `my-var` and `name`.