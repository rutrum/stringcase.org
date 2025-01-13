+++
title = "camelCase"
weight = 34
+++

_Camel case_ is the camel pattern with empty string delimiter.

## Synonyms

- _Camel caps_
- _Mixed case_
- _Lower camel case_, to distinguish it from [pascal case](../pascal).
- _Dromedary case_, also to distinguish it from [pascal case](../pascal), since dromedary camels have only one hump, comparable to the single upper case letter.
- _Camel back_
- _Compound Names_
- _Embedded Capitals_ or _Embedded Caps_
- _Bumpy case_ or _Bumpy caps_
- _Nerd caps_
- _Turtle case_
- _Smalltalk case_, in reference to the Smalltalk programming language **todo: verify**

**todo: figure out which of these are specific to lower camel case**
## Known Literature

Google's C++ style guide refers to camel case as mixed case, and further describes how you would define the words that compose an identifier, and then even mentions abbreviations. [^1]

> For the purposes of the naming rules below, a "word" is anything that you would write in English without internal spaces. This includes abbreviations, such as acronyms and initialisms. For names written in mixed case (also sometimes referred to as "camel case" or "Pascal case"), in which the first letter of each word is capitalized, prefer to capitalize abbreviations as single words, e.g., StartRpc() rather than StartRPC().

[^1]: [Google C++ Style Guide: General Naming Rules](https://google.github.io/styleguide/cppguide.html#General_Naming_Rules)

## Examples

Variables and functions in Java are written in camel case.

```java
public int addTwo(int a) {
    int numberPlusTwo = a + 2;
    return numberPlusTwo;
}
```
