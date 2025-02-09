+++
title = "camelCase"
slug = "../camel"
weight = 34
+++

_Camel case_ is the camel pattern with empty string delimiter.

Camel case is also known as _mixed case_ or _lower camel case_ (to distinguish it from [pascal case](../pascal)).

## History

Google's C++ style guide refers to camel case as mixed case, and further describes how you would define the words that compose an identifier, and then even mentions abbreviations. [^1]

> For the purposes of the naming rules below, a "word" is anything that you would write in English without internal spaces. This includes abbreviations, such as acronyms and initialisms. For names written in mixed case (also sometimes referred to as "camel case" or "Pascal case"), in which the first letter of each word is capitalized, prefer to capitalize abbreviations as single words, e.g., StartRpc() rather than StartRPC().

They also use mixed case to refer to both camel case and pascal case.  Google further uses _mixed caps_ to describe this case in its Go style guide. [^2]

> Go source code uses MixedCaps or mixedCaps (camel case) rather than underscores (snake case) when writing multi-word names.

Interestingly, Go uses pascal case and camel case to not only distinguish between exported and unexported identifiers, but also permit variables to be exported by enforcing pascal case.  This clear distinction of intent between the two is fascinating, given that the guide exclusively uses the name mixed caps to refer to both.

[^1]: [Google C++ Style Guide: General Naming Rules](https://google.github.io/styleguide/cppguide.html#General_Naming_Rules)
[^2]: [Google Go Style Guide: Core Guidelines](https://google.github.io/styleguide/go/guide#mixedcaps)

## Examples

Variables and functions in Java are written in camel case.

```java {filename="Java"}
public int addTwo(int a) {
    int numberPlusTwo = a + 2;
    return numberPlusTwo;
}
```

In Go, unexported identifiers like local and private variables and functions are written in camel case.
```go {filename="Go"}
package main

import "fmt"

type person struct {
    name string
    age  int
}

func newPerson(name string) *person {
    p := person{name: name}
    p.age = 24
    return &p
}

func main() {
    fmt.Println(person{"Alice", 20})
}
```
