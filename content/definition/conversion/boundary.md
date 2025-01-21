+++
title = "Boundary"
weight = 12
+++

We say a _boundary_ is some condition that splits an identifier into a list of words.

Some boundaries _discard_ some substring at the location of an identified boundary, and others do not.

A boundary consists of three parts:
* the condition: a function that takes a slice of the identifier starting at location `i` to the end of the identifier, and returns it true if the boundary condition is met
* the index of the start of boundary `start` relative to the slice of the identifier
* the length of the boundary `len`

To identify the locations of an identifier that contain boundaries, we iterate through substrings of the identifier.  For `i` from 0 to the length of identifier `I`, we create a slice `S = I[i:]`.  If this slice meets the condition, we have identified a split in the identifier.  The end of the previous word is at index `i+start` exclusive and the start of the next word is at index `i+start+len` inclusive.

## Splitting

We say _splitting_ is the process of converting an identifier into a list of words.

In pseudocode, you could implement splitting by a boundary `b` as follows.

```
function split(b: Boundary) {
    words = []
    last_word_start = 0

    for i in 0..n {
        S = I[i:]
        if b.condition(S) {
            last_word_end = i + b.start
            words.append( I[last_word_start:last_word_end] )
            last_word_start = i + b.start + b.len
        }
    }
    words.append(I[last_word_start:])

    return words
}
```

## Delimiter Example

Suppose we wanted to split a snake case identifier into words.  The boundary can be defined as follows:

* `condition`: is the first character in the slice equal to an underscore? `S[0] == "_"`
* `start`: 0
* `len`: 1

Examine the identifier `I = last_byte_count`.  This boundary condition would be true at index 4.  This means the start of the boundary would be at 4 + start, or 4.  The length of the boundary is 1, so the end of the boundary is 4 + 1, or 5.  Using these values to split the word, we would get `I[:4] = last` and `I[5:] = byte_count`.  We would continue until we reach the end of the string.

## Camel Case Example

Camel case is delimited by an empty string.  We can define the boundary as follows:

* `condition`: is the first character lowercase and the second character uppercase? `S[0].is_upper() and S[1].is_lower()`
* `start`: 1
* `len`: 0

Because our condition checks the character before and after the split, we set a start of 1.  And we don't want to remove any characters while splitting, so the length is 0.