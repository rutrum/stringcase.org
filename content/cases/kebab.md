+++
title = "kebab-case"
weight = 20
+++

_Kebab case_ is the lower pattern with the hyphen `-` delimiter.

## Synonyms

- _Dash case_[^1] or _Hyphen case_[^2]
- _List case_[^1]
- _Spinal case_[^1]
- _Caterpillar case_[^2]
- _Param case_[^2]
- _Lisp case_[^1], in reference to the Lisp programming language

[^1]: [Nishanth J., answering: What are the different kinds of cases?](https://stackoverflow.com/a/64293621)
[^2]: [Andreas Herz, answering: What are the different kinds of cases?](https://stackoverflow.com/a/54330161)

## History

While the usage of kebab case has been around for a long time, the earliest known record of its name dates to July 23, 2013 by user Ben Lee in [this stackoverflow post](https://stackoverflow.com/questions/11273282/whats-the-name-for-hyphen-separated-case).

## Usage

Kebab case is used in HTML/CSS as class and id names.

```html
<div class="large-box">
    <span id="page-title">Welcome!</span>
</div>
```

Lisp also uses kebab case for most identifiers.[^1]

```lisp
(when (engine-running-p car)
  (drive car))

(unless (seatbelts-fastened-p car)
  (warn-passengers car))
```

It is not commonly used as identifiers for variables or functions in programming languages because the hyphen `-` is used to represent subtraction, and can't be used in identifiers.

[^1]: [Lisp Style Guide](https://lisp-lang.org/style-guide/#naming)