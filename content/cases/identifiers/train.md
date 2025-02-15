+++
title = "Train-Case"
slug = "../train"
weight = 25
+++

_Train case_ is the capital pattern with hyphen delimiter.

## Usage

This is the case commonly used for HTTP Headers, although the HTTP specification does not require headers be in a particular case.[^1]

```
GET /cases/train/ HTTP/1.1
Host: stringcase.org
User-Agent: Mozilla/5.0...
Accept: text/html,application/xhtml+xml,...
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br, zstd
```

PowerShell also uses this extensively for all of its _cmdlets_, or native commands available within PowerShell.

```ps1 {filename="PowerShell"}
Get-Process | Get-Member | Out-Host -Paging
```

[^1]: [RFC 2615](https://www.rfc-editor.org/rfc/rfc2616#section-4.2)
