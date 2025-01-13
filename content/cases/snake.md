+++
title = "snake_case"
weight = 10
+++

_Snake case_ is the lower pattern with underscore `_` delimiter.

## Synonyms

- _Lowercase with underscores_

## Known Literature

The python standard library describes snake case as follows. [^1]

> The following naming styles are commonly distinguished.
>
> ...
>
> * `lower_case_with_underscores`

[^1]: [PEP-0008 Naming Styles](https://peps.python.org/pep-0008/#descriptive-naming-styles)

## Examples

Python and rust use snake case identifiers for function names.

```python
def add_two(a):
    return a + 2
```

```rust
fn add_two(a: int) -> int {
    a + 2
}
```
