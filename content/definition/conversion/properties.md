+++
title = "Conversion Properties"
weight = 13
math = true
+++

We say that a converter is _invertible_ if can be applied with reverse cases to get the same instance back.

Suppose we have some converter with parameters case $x$ and case $y$ called $C(x,y)$.  Then C is invertible if $C(y,x, C(x,y,I)) = I$.
