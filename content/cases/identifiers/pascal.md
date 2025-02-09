+++
title = "PascalCase"
slug = "../pascal"
weight = 33
+++

_Pascal case_ is the capital pattern with empty string delimiter.

Pascal case is also known as _upper camel case_.

## History

Pascal programming language.

## Examples

Rust uses Pascal case for struct, enum, and trait names.

```rust {filename="Rust"}
enum Answer {
    MoreThanOnce,
    ExactlyOnce,
    Never,
}

impl TryFrom<i32> for Answer {
    type Error = ();

    fn try_from(num: i32) -> Result<Self, Self::Error> {
        match num {
            i if i == 0 => Ok(Answer::Never),
            i if i == 1 => Ok(Answer::ExactlyOnce),
            i if i > 1 => Ok(Answer::MoreThanOnce),
            _ => Err(()),
        }
    }
```
