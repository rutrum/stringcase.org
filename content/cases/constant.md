+++
title = "CONSTANT_CASE"
weight = 11
+++

_Constant case_ is the upper pattern with underscore `_` delimiter.

## Synonyms

- _Upper snake case_ or _Screaming snake case_
- _upper snail case_ or _Screaming snail case_

## History

Constant refers to a property of variables in programming languages.  Constant variables never change value after being initialized.  In the C programming language, the convention is to write these variables in what we refer to as constant case.

Languages such as Java refer to this type of immutable variable as `final` but is cased the same.

## Examples

Many programming languages, like Java or C, use constant case for constants: variables with unchanging value.

```java
class Dog {
    public static final int NUM_LEGS = 4;
}
```

```c
const float PI = 3.14159;
```

C also uses constant case for macros, which are compile time evaluated blocks of code.

```c
#define PI 3.14159
```

Rust uses constant case for global variables, both immutable (`const`) and mutable (`static`).

```rust
static SITE_NAME: &str = "stringcase.org";
const PI: f32 = 3.14159;
```