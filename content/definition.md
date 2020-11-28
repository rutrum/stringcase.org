+++
title = "Definition"
+++

# Disclaimer

The following are notes for a smaller problem.  This example is still being refined so that a true formal construction can be defined.  The ultimate goal is to classify _conversion_ between string cases.  Is this an important problem to solve? Of course not.  But that is what this website has set out to do.

I encourage anyone reading to poke holes in the way the example is constructed.

<hr>

We will construct a small example that simplifies the case conversion problem.  Further analysis is required.

## Characters

A **character** is a ASCII symbol valued 65-90 `A-Z`, 97-122 `a-z`, 95 `_`, or 45 `-`.  We call this set of characters $C$.  We classify characters under three **character classes**:
* **uppercase**: `A-Z`
* **lowercase**: `a-z`
* **symbol**: `_` and `-`

We can write these characters as `'a'` or simply as `a`.  There is a one to one mapping of uppercase characters to lowercase characters.  Conversion between them will simply be "to make lowercase" or "to make uppercase".

*consider calling a word a grapheme?*

## Words

A **word** is a string of uppercase and lowercase letters such that the word lies within one of three **word cases**:
* An **uppercase** word contains only uppercase characters
* A **lowercase** word contains only lowercase characters
* A **capitalized** word starts with an uppercase character while the rest are lowercase

We will not consider lists of characters that do not fall within one of these cases.  We will call this set of words $W$.  Words can be abbreviated from a list of characters to simply the character concatenated with one another.  That is instead of writing `('a', 'b', 'c')` we could write `"abc"`, or even more simply `abc`.

We denote the case of a word $w$ as $w_c$.  Using the mapping from lowercase to uppercase letters, it should be clear to see that given any word we could convert to an appropriate word of another class.  For example the lowercase word `notebook` could be converted to uppercase `NOTEBOOK` or capitalized case `Notebook`.

## Delimeters

We define a **delimiter** as a set containing at most one symbol character.  Informally, we consider delimiters `-` and `_` as well as using no delimeter, or the empty `{}` delimeter.  We call the set of all delimiters $D$.  We call the set of non-empty delimeters $D^*$.

## Word Representation, Identifiers, and Joining

A list of words of the same case is called a **word representation**.  The pair of a word representation and a delimeter can be mapped into a string called an **identifier**.  Suppose we have a word representation $r$ of length $n$ and delimeter $d$.  We can concatenate $||$ as follows to construct an identifier $i$:
$$i = r_0  ||  d  ||  r_1  ||  d \dots d  ||  r_{n-1}$$

For example, suppose we have word representation `(my, var, name)` and delimeter `-`.  This would construct the identifier `my-var-name`.  The word representation `(MY, VAR, NAME)` and the empty delimeter would construct the identifier `MYVARNAME`.

We call the set of all identifiers $I$ and the set of all word representations as $R$.

We will call the function that maps a word representation and delimeter to an identifier $\mathcal{join}$.  Constructing a word representation and delimeter from an identifer is called $\mathcal{segmentation}$.  Note that not any string is an identifier, only those strings that are joined from a word representation and delimeter.

$$
\begin{aligned}
\mathcal{segment} &: I \rightarrow (R, D) \\\\
\mathcal{join} &: (R, D) \rightarrow I
\end{aligned}
$$

As will be discussed in detail later, this functions are not inverses of one another.  The word case of all the words in a word representation $r$ is denoted $r_c$.  The join function was clearly defined, but the segmentation function is more complicated.  The goal of the segmentation function is to construct a word representation and delimeter from an identifier such that that when joined is equal to the identifier.  Before defining this function, we must discuss identifier casing.

Observations:
* Every word is an identifier.

## Cases

We define an **identifier case** or **string case** or simply **case** as an order pair (*word case*, *delimeter*).  There are nine such cases, each with a unique name.  They are listed in the following table.

| | $\\{\\_\\}$ | $\\{-\\}$ | $\\{\\}$ |
| --- | --- | --- | --- |
| **lowercase** $aa$ | snake_case | kebab-case | flatcase |
| **uppercase** $AA$ | UPPER_SNAKE_CASE | COBOL-CASE | UPPERFLATCASE |
| **capitalized** $Aa$ | Pascal_Snake_Case | Train-Case | PascalCase |

Identifiers can be associated with a case based on the word representation and delimeter found from the segmentation function.  Every identifier is one of the above cases. That is, for some identifier $i$, with $\mathcal{segment}(i) = (r, d)$, the case of $i$ is
$$(r_c, d).$$

## Segmentation

If an identifier is joined using a nonempty delimeter, the segmentation function is well defined.  It is unambiguous were to put word boundaries to construct the word representation.  

However, if the identifier is joined using the empty delimeter and a word representation that is uppercase or lowercase, there are many ways to segment the identifier.  For example, `(my, var, name)` can be joined with the empty delimeter to construct `myvarname`.  This could be segmented in many ways, such as `(my, var, name)`, `(myvar, name)`, or `(m, yvarname)`.  

We choose to define our segmentation function for these cases.  That is, for `flatcase` and `UPPERFLATCASE` identifiers $i$, we define the segmentation function to yield the word representation of length 1 with empty delimeter.
$$\mathcal{segment}(i) = ((i), \{\}).$$

It should be clear to see that segmenting an identifier of any other case is unambiguous.

## Case Conversion

We call **case conversion** the process of changing an identifier's case.  That is, it is the combination of segmenting the identifier, converting the word representations case, and joining using the appropriate delimeter.  The algorithm is as follows, for converting an identifier $i$ into case $c$.
1) Let $\mathcal{segment}(i) = (r, d^*)$.
2) Let $c$ = $(w_c, d)$.
3) Construct $r'$ by converting each word of $r$ into word case $w_c$.
4) Return $\mathcal{join}(r', d)$.

The interesting part comes when converting from one case into another, and then back again.  That is, when converting an identifier into `flatcase` or `UPPERFLATCASE`, information is lost and it cannot always be converted back into the original identifier.  The information lost is in the underlying identifier's word representation.  That is, our segmentation function is not always accurate when segmenting identifiers in `flatcase` or `UPPERFLATCASE`.

