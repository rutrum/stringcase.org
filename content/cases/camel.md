+++
title = "camelCase"
weight = 34
+++

_Camel case_ is the camel pattern with empty string delimiter.

## Synonyms

- _Camel caps_
- _Mixed case_[^1]
- _Lower camel case_, to distinguish it from [pascal case](../pascal).
- _Dromedary case_[^2], also to distinguish it from [pascal case](../pascal), since dromedary camels have only one hump[^3], comparable to the single upper case letter.
- _Camel back_[^4]
- _Compound Names_[^5]
- _Pothole case_[^6]
- _Embedded Capitals_[^7] or _Embedded Caps_[^8]
- _Bumpy case_ or _Bumpy caps_[^8]
- _Nerd caps_[^8]
- _Turtle case_[^8]
- _C case_[^2]
- _Smalltalk case_, in reference to the Smalltalk programming language **todo: verify**

**todo: figure out which of these are specific to lower camel case**

[^1]: [Style Guide for Python Code: Naming Styles](https://peps.python.org/pep-0008/#descriptive-naming-styles)
[^2]: [Nishanth J., answering: What are the different kinds of cases?](https://stackoverflow.com/a/64293621)
[^3]: [National Geographic: Arabian Camel (Dromedary)](https://www.nationalgeographic.com/animals/mammals/facts/arabian-camel)
[^4]: [Purdue University: C# Coding Standards and Guidelines](https://web.archive.org/web/20080411055228/http://www2.tech.purdue.edu/cit/Courses/CPT355/C_Sharp_Coding_Standards_and_Guidelines.asp)
[^5]: [Ian Feldman: compoundNames](https://groups.google.com/group/alt.folklore.computers/browse_thread/thread/6099191f2c4e0984/21f332e5b813313e?#21f332e5b813313e)
[^6]: [Michael Guerzhoy: Variable Naming Conventions](https://www.cs.toronto.edu/~guerzhoy/180f16/lectures/W02/lec2/VariableNamingConvetions.html)
[^7]: [Dwight Harn: If class name has embedded capitals, AppGen code fails UI tests, and generated hyperlinks are incorrect.](https://web.archive.org/web/20170625073321/http://issues.appfuse.org/browse/APF-1088)
[^8]: [Michelle Rau: CamelCase: It's a thing](https://michellerau.com/2017/03/25/camelcase-its-a-thing/)

## Known Literature

Google's C++ style guide refers to camel case as mixed case, and further describes how you would define the words that compose an identifier, and then even mentions abbreviations. [^9]

> For the purposes of the naming rules below, a "word" is anything that you would write in English without internal spaces. This includes abbreviations, such as acronyms and initialisms. For names written in mixed case (also sometimes referred to as "camel case" or "Pascal case"), in which the first letter of each word is capitalized, prefer to capitalize abbreviations as single words, e.g., StartRpc() rather than StartRPC().

[^9]: [Google C++ Style Guide: General Naming Rules](https://google.github.io/styleguide/cppguide.html#General_Naming_Rules)

## Examples

Variables and functions in Java are written in camel case.

```java
public int addTwo(int a) {
    int numberPlusTwo = a + 2;
    return numberPlusTwo;
}
```
