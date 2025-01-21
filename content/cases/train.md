+++
title = "Train-Case"
weight = 25
+++

_Train case_ is the capital pattern with hyphen delimiter.

## History

The HTTP specification does not require that HTTP Headers be in a particular case.[^1]

[^1]: [RFC 2615](https://www.rfc-editor.org/rfc/rfc2616#section-4.2)

## Usage

This is the case used for HTTP Headers.

```
GET /cases/train/ HTTP/1.1
Host: stringcase.org
User-Agent: Mozilla/5.0...
Accept: text/html,application/xhtml+xml,...
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br, zstd
```
