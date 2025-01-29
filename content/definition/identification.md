---
title: Case Identification
---

What does it mean for an identifier to _have_ a case?  Can an identifier inherantly present itself as being formatted as a case?

It is immediately apparent that an identifier can look like many cases.  Any flatcase word can look like any lowercase patterned case.  Any single word can be associated with any case that follows similar word pattern.

## Is the identifier a fixed point in converting to target case?

Instead of detecting case, let's first check if an identifier I is formatted as a case C.  You might first ask, if we convert I into another identifier under the case C, is it the same?  That might motivate that the identifier is already formatted as a case C.

But to convert into a case C not only depends on C, but also a set of boundary conditions B.  What boundaries should be chosen?  If we were to choose the boundaries associated with a case, we can generate a counter example.

Convert `kebab-case-string` into snake case.  If we just split on underscore, we would get a single word.  Converting to snake case would mean making all letters lowercase, which makes no changes.  Further, no joining is necessary since one word was identified.  In this scenario, we cannot simply use the boundaries associated with the target case.

What makes this problem difficult is that we do not know the current case of the string for splitting into words.  If we did, then this identification would not be necessary.

What if we applied all boundaries?  Assume that the identifier could be any case, so we try splitting by every common set of boundaries.  If _all_ conversions are identified as the target case, then it is the target case.  `drumStickString`.  Is this snake?  Well, splitting by lowercase letter followed by uppercase letter would be yield 3 words, which are not joined by underscores, so we know it is not snake case.  We can visually see that this is camel case.  I think everything would fail here.

Is there a counter example for this?  I think I will need to actually implement this in convert-case tests and see.

## Checking letter by letter casing and boundaries

What if we check based on qualities of converted identifiers?  For instance, we know that snake case has only lowercase letters and underscores.  If any other symbol is present, then we know it is not snake case.

The problem with this approach is that it assumes that we know the full list of cases it _can't_ be.  That may not be fair.  In some world, we could call `this.ident.ifier` snake case, but it's actually dot case to someone else.

Symbols are another issue here.  **To check if something is a case, we cannot ignore symbols**.  Having symbols that are not present in the delimiter would make the identifier not a certain case.

We can enforce no symbols.  Let's say this.  An identifier is a case _C_ if
1. all characters either have a case, or are the case's delimiter, and
2. letters are either all upper, all lower, or a mixture depending on the output of the case's pattern.

`kebab-case-string` immediately fails number 1 for snake case, since it contains hyphens.  `thisidentifier` is also snake case, of one word.

## Heuristic Approach

What if a string earned "points" for each case, and the case that had the most points was considered the best.  This assumes there a base list of cases of which to pick from.

## Boundary Detection

This really is a question of boundary detection, but we also check symbol presence.  The conversion method works if we were to remove or detect symbols not present in the delimiter.  This raises the question about numbers, as well.  But I don't suspect numbers being used as a delimiter.

But this does make the assumption that the set of possible boundaries are distinct from letters.  I would like to continue flying with the assumption that a boundary is any string, not just symbols.
