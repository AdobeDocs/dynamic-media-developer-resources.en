---
title: Image Rendering HTTP encoding
description: Command values must be http-encoded using %xx escape sequences, such that the value strings do not include the reserved characters '=', '&', and '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
---
# Image Rendering HTTP encoding{#image-rendering-http-encoding}

Command values must be http-encoded using %xx escape sequences, such that the value strings do not include the reserved characters '=', '&', and '%'.

Otherwise, standard HTTP encoding rules apply. The HTTP specification requires encoding of the unsafe characters such as ' ' (space), '"'(double-quote), '#', '%', '<', and '>', as well as any control characters, such as `<return>` and `<tab>`.

**Caution:** Curly braces { } used as request-nesting delimiters must not be encoded. Certain email clients unfortunately encode curly braces in embedded HTTP request. Should this issue be a problem, Image Rendering allows use of parentheses ( ) instead of curly braces.

## Example {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

The above request fragment must be encoded as follows:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## See also {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 Specification (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
