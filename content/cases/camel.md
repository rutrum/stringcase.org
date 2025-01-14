+++
title = "camelCase"
weight = 34
+++

_Camel case_ is the camel pattern with empty string delimiter.

## Synonyms

- _Camel caps_
- _Mixed case_[^1]
- _Lower camel case_, to distinguish it from [pascal case](../pascal).
- _Dromedary case_, also to distinguish it from [pascal case](../pascal), since dromedary camels have only one hump[^2], comparable to the single upper case letter.
- _Camel back_[^3]
- _Compound Names_[^4]
- _Embedded Capitals_[^5] or _Embedded Caps_[^6]
- _Bumpy case_ or _Bumpy caps_[^6]
- _Nerd caps_[^6]
- _Turtle case_[^6]
- _Smalltalk case_, in reference to the Smalltalk programming language **todo: verify**

**todo: figure out which of these are specific to lower camel case**

[^1]: [Style Guide for Python Code: Naming Styles](https://peps.python.org/pep-0008/#descriptive-naming-styles)
[^2]: [National Geographic: Arabian Camel (Dromedary)](https://www.nationalgeographic.com/animals/mammals/facts/arabian-camel)
[^3]: [Purdue University: C# Coding Standards and Guidelines](https://web.archive.org/web/20080411055228/http://www2.tech.purdue.edu/cit/Courses/CPT355/C_Sharp_Coding_Standards_and_Guidelines.asp)
[^4]: [Ian Feldman: compoundNames](https://groups.google.com/group/alt.folklore.computers/browse_thread/thread/6099191f2c4e0984/21f332e5b813313e?#21f332e5b813313e)
[^5]: [Dwight Harn: If class name has embedded capitals, AppGen code fails UI tests, and generated hyperlinks are incorrect.](https://web.archive.org/web/20170625073321/http://issues.appfuse.org/browse/APF-1088)
[^6]: [Michelle Rau: CamelCase: It's a thing](https://michellerau.com/2017/03/25/camelcase-its-a-thing/)

## Known Literature

Google's C++ style guide refers to camel case as mixed case, and further describes how you would define the words that compose an identifier, and then even mentions abbreviations. [^7]

> For the purposes of the naming rules below, a "word" is anything that you would write in English without internal spaces. This includes abbreviations, such as acronyms and initialisms. For names written in mixed case (also sometimes referred to as "camel case" or "Pascal case"), in which the first letter of each word is capitalized, prefer to capitalize abbreviations as single words, e.g., StartRpc() rather than StartRPC().

[^7]: [Google C++ Style Guide: General Naming Rules](https://google.github.io/styleguide/cppguide.html#General_Naming_Rules)

## Examples

Variables and functions in Java are written in camel case.

```java
public int addTwo(int a) {
    int numberPlusTwo = a + 2;
    return numberPlusTwo;
}
```
