+++
title = "About"
type = "default"
sidebar.exclude = true
+++

This project started because I wanted a command line utility that would turn snake cased filenames into title cased strings to present in an interactive prompt for selecting the file.  I wrote a Rust library called `convert-case` and then a command line utility on top of it called `ccase`.

In the process of writing the library I noticed that case conversion libraries all use different naming conventions for each case.  They can also have a limited selection of cases, forcing you to use standard string methods to perform more conversion.  Many don't have documented or consistent behavior for edge cases, like how to handle digits.  And lastly, they didn't give you any freedom to choose how the original string was split in the the first place.

So alongside the development of `convert-case`, I took notes to formalize the process for doing robust case conversion.  I created this site to document my definition of a case, so that other libraries could implement a standard set of cases and robust behavior.

The definition and terminology are highly inspired by most people's exposure to these ideas: programmming languages.  While the nature of how you combine multiple words into a single token without whitespace is generic, it's usage is frequent in programming and the authors of programming languages and the programming community use names to refer to formatting.  It is for this reason most language is centered around terminology used in compilation.

This site is a work in progress.
