+++
title = "kebab-case"
slug = "../kebab"
weight = 20
+++

_Kebab case_ is the lower pattern with the hyphen `-` delimiter.

Kebab case is also known as _dash case_ or _hyphen case_.

## History

## Naming

While the usage of kebab case has been around for a long time, the earliest known record of its name dates to July 23, 2013 by user Ben Lee in [this stackoverflow post](https://stackoverflow.com/questions/11273282/whats-the-name-for-hyphen-separated-case).

## Usage

Kebab case is used in HTML/CSS as class and id names.

```html {filename="HTML"}
<div class="large-box">
    <span id="page-title">Welcome!</span>
</div>
```

Lisp also uses kebab case for most identifiers.[^1]

```lisp {filename="Lisp"}
(when (engine-running-p car)
  (drive car))

(unless (seatbelts-fastened-p car)
  (warn-passengers car))
```

It is not commonly used as identifiers for variables or functions in programming languages because the hyphen `-` is used to represent subtraction, and can't be used in identifiers.

It is also common practice to use kebab case for the path in the url.

[^1]: [Lisp Style Guide](https://lisp-lang.org/style-guide/#naming)
