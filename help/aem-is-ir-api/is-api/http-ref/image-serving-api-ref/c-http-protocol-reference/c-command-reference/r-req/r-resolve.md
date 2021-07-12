---
description: Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog Modifier inclusions, macro and variable substitutions, etc, just like req=img.
solution: Experience Manager
title: resolve
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
---
# resolve{#resolve}

Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog::Modifier inclusions, macro and variable substitutions, etc, just like req=img.

 `req=resolve`

The final request string is returned, instead of the result image, with MIME type `text/plain`.

The HTTP response is not cacheable.
