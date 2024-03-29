---
title: Variable processing in embedded foreign requests
description: $var$ references occurring anywhere within the curly braces of an embedded foreign request are substituted with matching variable definition values.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
---
# Variable processing in embedded foreign requests{#variable-processing-in-embedded-foreign-requests}

Any `$var$` references that occur anywhere within the curly braces of an embedded foreign request are substituted with matching variable definition values.

Allows embedded foreign requests to be placed in a template in an image catalog.

Variable values which are to be substituted into foreign requests typically must be double-encoded, because no re-encoding is applied before the server attempts to transmit the final foreign url.
