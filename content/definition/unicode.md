+++
title = "Unicode"
weight = 100
+++

Here we broaden our previous intuition to include not just ASCII characters from the basic latin block, but all unicode code points.  This involves a re-definition of what lettercase is, as well as how we split identifiers based on boundaries.

In the context of how string cases are typically used (programming languages) limiting the definition to ASCII characters would be sufficient.  The stringcase standard might be split in multiple parts, where you can be ASCII compliant or Unicode compliant.

## Letter Case (?)

Unicode standard defines the following properties of code points.

> TODO: see chapter 4.2.1

## Boundaries

Segmentation of unicode code points into "graphs" (I dont recall what it is, grams?) is a complicated matter.

## Another non-unicode consideration

We should also introduce in this section how to respond to words that contain glyphs that are not just upper or lowercase letters.  What about numbers or symbols present?

I am tempted to define a "letter pool" that we assume upfront about what letters are present in a word...but that's most of them, and really it depends entirely on the delimiter.  If we assume a snake case identifier, we can assume a word contains all possible characters that aren't underscore explicitly.
