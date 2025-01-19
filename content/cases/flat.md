+++
title = "flatcase"
weight = 30
+++

_Flat case_ is the lower pattern with empty string delimiter.

## History

Google style guide: [^1]:

> Package names use only lowercase letters and digits (no underscores). Consecutive words are simply concatenated together. For example, com.example.deepspace, not com.example.deepSpace or com.example.deep_space.

[^1]: [Google Java Style Guide: Package names](https://google.github.io/styleguide/javaguide.html#s5.2.1-package-names)

Oracle style guide: https://docs.oracle.com/javase/tutorial/java/package/namingpkgs.html

Even the references on wikipedia's page for "flatcase" reference a stack overflow post and a random article.

## Examples

**Domain names, web things**  Think about protocols

Java package names are tied to a domain name, which are typically written in all lowercase, without symbols.  If a package is made for a prime seive data structure, the package name might be `primesieve`.
