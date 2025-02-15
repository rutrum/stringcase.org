+++
title = "PascalCase"
slug = "../pascal"
weight = 33
+++

_Pascal case_ is the capital pattern with empty string delimiter.

Pascal case is also known as _upper camel case_.

## History

Pascal is a case-insensitive language, so the same identifier can be referenced using a different mixture of upper and lowercase letters each time.

This document[^1] with footer dating it at 1998 suggests Pascal case for most identifiers, additionally describing prefixes to prepend to certain types. (**todo: figure out what what convention is called**).

This other document[^2] calls Pascal case _infix caps_.  It suggests using infix caps for all identifiers.

The GNU Pascal manual[^3], last updated in 2005, describes Pascal case as the following:

> Only the first letter should be capital, or, if there are concatenated words or acronyms, the first letter of each word should be capital – do not use underscores. 

Additionally, it comments on acronyms.

> Acronyms that have become part of the natural language can be written like that. 

[^1]: [Pascal Style and Format Guide from chairouchu.com](https://chairouchu.com/documents/Format01.pdf)
[^2]: [Object Pascal Style Guide Archive in 2017](https://ia800603.us.archive.org/18/items/ObjectPascalStyleGuide_201708/SoftwareEngineering/Object%20Pascal%20Style%20Guide.pdf)
[^3]: [GNU Pascal Coding Standards](https://www.gnu-pascal.de/h-gpcs-en.html)

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
